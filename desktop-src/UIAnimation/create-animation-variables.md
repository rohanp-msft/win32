---
title: Create Animation Variables
description: An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.
ms.assetid: 360aa157-cb50-400a-b373-45885410469d
keywords:
- animation variables Windows Animation ,creating
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Create Animation Variables

An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.

## Overview

Animation variables are created using the animation manager, and the application should retain a reference to each for as long as it is needed. Your application will generally create each animation variable at the same time as the visual object it animates.

When an animation variable is created, its initial value must be specified. Thereafter, its value can only be altered by scheduling storyboards that animate it.

Animation variables are passed as parameters when storyboards are constructed, so the application should not release them until the visual characteristics they represent no longer need to be animated, typically when the associated visual objects are about to be destroyed.

## Example Code

-   [Animating Colors](#animating-colors)
-   [Animating x and y Coordinates](#animating-x-and-y-coordinates)

### Animating Colors

The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md). In the example, three animation variables are created using [**CreateAnimationVariable**](/windows/win32/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable?branch=master) to represent background colors. The code also uses the [**SetLowerBound**](/windows/win32/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound?branch=master) and [**SetUpperBound**](/windows/win32/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound?branch=master) methods to control the value of the animation variable.


```
const DOUBLE INITIAL_RED = COLOR_MAX;
const DOUBLE INITIAL_GREEN = COLOR_MAX;
const DOUBLE INITIAL_BLUE = COLOR_MAX;

HRESULT hr = m_pAnimationManager->CreateAnimationVariable(
    INITIAL_RED,
    &amp;m_pAnimationVariableRed
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableRed->SetLowerBound(COLOR_MIN);
    if (SUCCEEDED(hr))
    {
        hr = m_pAnimationVariableRed->SetUpperBound(COLOR_MAX);
        if (SUCCEEDED(hr))
        {
            hr = m_pAnimationManager->CreateAnimationVariable(
                INITIAL_GREEN,
                &amp;m_pAnimationVariableGreen
                );
            if (SUCCEEDED(hr))
            {
                hr = m_pAnimationVariableGreen->SetLowerBound(COLOR_MIN);
                if (SUCCEEDED(hr))
                {
                    hr = m_pAnimationVariableGreen->SetUpperBound(COLOR_MAX);
                    if (SUCCEEDED(hr))
                    {
                        hr = m_pAnimationManager->CreateAnimationVariable(
                            INITIAL_BLUE,
                            &amp;m_pAnimationVariableBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            hr = m_pAnimationVariableBlue->SetLowerBound(COLOR_MIN);
                            if (SUCCEEDED(hr))
                            {
                                hr = m_pAnimationVariableBlue->SetUpperBound(COLOR_MAX);
                            }
                        }
                    }
                }
            }
        }
    }
}
```



Note the following definitions from MainWindow.h.


```
class CMainWindow
{

    ...

private:

    // Animated Variables

    IUIAnimationVariable *m_pAnimationVariableRed;
    IUIAnimationVariable *m_pAnimationVariableGreen;
    IUIAnimationVariable *m_pAnimationVariableBlue;

    ...

};
```



### Animating x and y Coordinates

The following example code is taken from Thumbnail.cpp in the Windows Animation [Grid Layout Sample](https://msdn.microsoft.com/library/windows/desktop/dd940512); see the CMainWindow::CreateAnimationVariables method. Two animation variables are created to represent the X and Y coordinates of each object.


```C++
// Create the animation variables for the x and y coordinates

hr = m_pAnimationManager->CreateAnimationVariable(
    xInitial,
    &amp;m_pAnimationVariableX
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->CreateAnimationVariable(
        yInitial,
        &amp;m_pAnimationVariableY
        );

    ...

}
```



Note the following definitions from Thumbnail.h.


```
class CThumbnail
{
public:

    ...

    // X and Y Animation Variables

    IUIAnimationVariable *m_pAnimationVariableX;
    IUIAnimationVariable *m_pAnimationVariableY;

    ...

};
```



Animation variables are floating-point numbers, but their values can be fetched as integers, too. By default, each value will be rounded to the nearest integer, but it is possible to override the rounding mode used for a variable. The following example code uses the [**SetRoundingMode**](/windows/win32/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode?branch=master) method to specify that the values should always be rounded down.


```C++
hr = m_pAnimationVariableX->SetRoundingMode(
    UI_ANIMATION_ROUNDING_MODE_FLOOR
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableY->SetRoundingMode(
        UI_ANIMATION_ROUNDING_MODE_FLOOR
        );

    ...

}
```



## Previous Step

Before starting this step, you should have completed this step: [Create the Main Animation Objects](adding-animation-to-an-application.md).

## Next Step

After completing this step, the next step is: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).

## Related topics

<dl> <dt>

[**IUIAnimationManager::CreateAnimationVariable**](/windows/win32/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable?branch=master)
</dt> <dt>

[**IUIAnimationVariable::SetLowerBound**](/windows/win32/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound?branch=master)
</dt> <dt>

[**IUIAnimationVariable::SetRoundingMode**](/windows/win32/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode?branch=master)
</dt> <dt>

[**IUIAnimationVariable::SetUpperBound**](/windows/win32/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound?branch=master)
</dt> <dt>

[Windows Animation Overview](scenic-animation-api-overview.md)
</dt> </dl>

 

 



