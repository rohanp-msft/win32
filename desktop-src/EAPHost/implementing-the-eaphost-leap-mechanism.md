---
title: Implementing the EAPHost LEAP Mechanism
description: Describes the EAPHost mechanism that allows third parties to write Lightweight Extensible Authentication Protocol (LEAP) modules for Windows.
ms.assetid: d17a99cb-4a43-4719-984e-b742c9518f52
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Implementing the EAPHost LEAP Mechanism

This topic describes the EAPHost mechanism that allows third parties to write Lightweight Extensible Authentication Protocol (LEAP) modules for Windows. LEAP is a legacy authentication method, created by Cisco, as per [RFC 3748](Http://go.microsoft.com/fwlink/p/?linkid=84016). For more information about LEAP, see [Cisco LEAP Q&A](Http://go.microsoft.com/fwlink/p/?linkid=84018).

## EAPHost Authentication Process

The regular EAPHost authentication process occurs as follows:

-   The authenticator sends a Request to authenticate the peer. For example, the application calls [**EapHostPeerBeginSession**](/windows/previous-versions/eappapis/nf-eappapis-eaphostpeerbeginsession?branch=master) with EAPHost configuration and user data.
-   The peer sends a Response packet in reply to a valid Request. For example, a successful call returns an **EAP\_SESSION\_HANDLE** session handle.
-   The authenticator sends an additional Request packet, and the peer replies with a Response. For example, the application calls [**EapHostPeerGetSendPacket**](/windows/previous-versions/eappapis/nf-eappapis-eaphostpeergetsendpacket?branch=master) to obtain EAP packets received by EAPHost throughout the session. Each packet is processed by a call to [**EapHostPeerProcessReceivedPacket**](/windows/previous-versions/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket?branch=master).
-   [**EapHostPeerProcessReceivedPacket**](/windows/previous-versions/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket?branch=master) will always return an action code. The supplicant must then call the function corresponding to the action code.
-   The sequence of Requests and Responses continues as long as needed. For example, the application can call [**EapHostPeerGetResponseAttributes**](/windows/previous-versions/eappapis/nf-eappapis-eaphostpeergetresponseattributes?branch=master) to request available EAP attributes, and the peer responds with [**EapHostPeerSetResponseAttributes**](/windows/previous-versions/eappapis/nf-eappapis-eaphostpeersetresponseattributes?branch=master) to return them.
-   After an initial Request, a new Request cannot be sent until a valid Response is received.
-   The conversation continues until the authenticator cannot authenticate the peer, in which case the authenticator implementation must transmit an EAP Failure. For example, unacceptable Responses to one or more Requests would cause the authenticator to transmit a Code 4 EAP Failure.
-   Alternatively, the authentication conversation can continue until the authenticator determines that successful authentication has occurred, in which case the authenticator must transmit an EAP Success (Code 3).
-   Whether the result indicates success or failure, the application calls [**EapHostPeerEndSession**](/windows/previous-versions/eappapis/nf-eappapis-eaphostpeerendsession?branch=master) to terminate the session. In the case of failure, re-authentication can be attempted by opening another session with EAPHost and providing either the same or a new identity.

### LEAP Authentication Process

The LEAP authentication process differs from the regular EAPhost authentication process as follows:

-   EAP authentication is initiated by the server (authenticator). LEAP, in contrast, is initiated by the client (peer).
    -   Therefore, when writing a LEAP module you must always ensure that the Challenge Request packet from the peer method and the EAP Response from the EAP server must always have the same packet ID as that of the EAP Success packet from the server.

    <!-- -->

    -   In contrast, EAPHost Request and Response and Success packets typically all have different IDs.
        > [!Note]  
        > Every EAP Request has a Type field to indicate what is being requested. As with the Request packet, every EAP Response packet contains a Type field, which corresponds to the Type field of the Request. Examples include Identity Request and Challenge Request packets.

         

-   In the case of failure with EAPHost, re-authentication can be attempted by opening another session with EAPHost and providing either the same identity or a new identity.

### LEAP Authenticator Method Implementation

When developing a LEAP authenticator method, please ensure the following:

-   LEAP authenticator methods must return the [**EAP\_METHOD\_AUTHENTICATOR\_RESPONSE\_SEND**](/windows/previous-versions/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-_eap_method_authenticator_response_action?branch=master) action code after the 1st phase of authentication (peer authentication) is successful. Then when [**EapMethodAuthenticatorSendPacket**](/windows/previous-versions/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket?branch=master) is called, it should return a valid [**EapPacket**](/windows/previous-versions/eapmethodtypes/ns-eapmethodtypes-tageappacket?branch=master) with an EAP code of [**EapCodeSuccess**](/windows/previous-versions/eapmethodtypes/ne-eapmethodtypes-tageapcode?branch=master).
-   LEAP authenticator methods should return the [**EAP\_METHOD\_AUTHENTICATOR\_RESPONSE\_RESULT**](/windows/previous-versions/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-_eap_method_authenticator_response_action?branch=master) action code if the 1st phase of peer authentication is unsuccessful.
-   LEAP authenticator methods must return the final authentication response packet with the [**EAP\_METHOD\_AUTHENTICATOR\_RESPONSE\_RESULT**](/windows/previous-versions/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-_eap_method_authenticator_response_action?branch=master) action code when [**EapMethodAuthenticatorSendPacket**](/windows/previous-versions/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket?branch=master) is called. Then in subsequent calls to [**EapMethodAuthenticatorGetResult**](/windows/previous-versions/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult?branch=master) the **EAP\_SESSION\_HANDLE** must be returned to identify the authenticated session.
-   

### LEAP Peer Method Implementation

When developing a LEAP peer method, please ensure the following

-   LEAP peer methods should return the [**EapPeerMethodResponseActionSend**](/windows/previous-versions/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-tageappeermethodresponseaction?branch=master) action code after the 1st phase of authentication (peer authentication) is successful.
-   LEAP peer methods should return the [**EapPeerMethodResponseActionResult**](/windows/previous-versions/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-tageappeermethodresponseaction?branch=master) action code after the 2nd phase of authentication is successful.

## Related topics

<dl> <dt>

[EAPHost Call Sequence](about-eaphost-call-sequences.md)
</dt> <dt>

[Using EAPHost](using-eap-host.md)
</dt> </dl>

 

 



