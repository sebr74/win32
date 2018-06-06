---
Description: The get\_DestinationLeft method retrieves the left coordinate of the current destination rectangle.
ms.assetid: f1c6d784-7ec3-4d44-a3fb-c1e3b988e392
title: CBaseControlVideo.get\_DestinationLeft method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# CBaseControlVideo.get\_DestinationLeft method

The `get_DestinationLeft` method retrieves the left coordinate of the current destination rectangle.

## Syntax


```C++
HRESULT get_DestinationLeft(
   long *pDestinationLeft
);
```



## Parameters

<dl> <dt>

*pDestinationLeft* 
</dt> <dd>

Pointer to the left coordinate of the destination rectangle.

</dd> </dl>

## Return value

Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.



| Return code                                                                                           | Description                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E\_FAIL**</dt> </dl>                | Failure.<br/>                                                              |
| <dl> <dt>**E\_POINTER**</dt> </dl>             | **NULL** pointer argument.<br/>                                            |
| <dl> <dt>**VFW\_E\_NOT\_CONNECTED**</dt> </dl> | The operation cannot be performed because the pins are not connected.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Success.<br/>                                                              |



 

## Remarks

This member function implements the [**IBasicVideo::get\_DestinationLeft**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft) method.

An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface. The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played. The destination rectangle is relative to the client area of the window in which it is playing. The upper-left corner of the window is coordinate (0,0).

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBaseControlVideo Class**](cbasecontrolvideo.md)
</dt> </dl>

 

 



