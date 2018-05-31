---
Description: Sending COPP Commands
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Sending COPP Commands
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Sending COPP Commands

To send a Certified Output Protection Protocol (COPP) command, fill in an [**AMCOPPCommand**](/windows/win32/strmif/ns-strmif-_amcoppcommand?branch=master) structure as follows:

-   **guidCommandID**. The GUID that identifies the command. See the COPP Command Reference.
-   **dwSequence**. The command sequence number. Increment this value after each command. (This value is shown as **uCommandSeq** in [Initiating a COPP Session](initiating-a-copp-session.md).)
-   **cbSizeData**. The size, in bytes, of any data needed for the command.
-   **CommandData**. Data for the command.

After you have filled in this data, calculate the MAC for the command:

1.  Calculate the OMAC-1 tag for the block of data that appears after the **macKDI** member of the **AMCOPPCommand** structure.
2.  Copy this value into the **macKDI** member of the structure.

Now pass the structure to the [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/win32/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand?branch=master) method.

## Related topics

<dl> <dt>

[Using Certified Output Protection Protocol (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 


