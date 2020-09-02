---
layout: post
title:  "QRCode with SpringBoot and Quarkus"
description: java qrcode springboot quarkus
date:   2020-09-01 16:00:00 +0530
categories: java QRCode Quarkus springboot
---

There are many types of BarCodes. In the below examples i was created QRCodes with zxing one library of Google.

So let's code:

With SpringBoot i get return image directly:

```
@GetMapping(value = "/1/{name}", produces = MediaType.IMAGE_PNG_VALUE)
public ResponseEntity<BufferedImage> barbecueEAN13Barcode(@PathVariable("name") String name) throws Exception {
    QRCodeWriter qrCodeWriter = new QRCodeWriter();
    BitMatrix bitMatrix = qrCodeWriter.encode(name, BarcodeFormat.QR_CODE, 200, 200);
    
    return okResponse(MatrixToImageWriter.toBufferedImage(bitMatrix));
}

private ResponseEntity<BufferedImage> okResponse(BufferedImage image) {
    return new ResponseEntity<>(image, HttpStatus.OK);
}
```

But with Quarkus i get only if base64, :(, but just recovert image:

```
    @GET
    @Produces(MediaType.TEXT_PLAIN)
    public String hello() throws WriterException, IOException {
        QRCodeWriter barcodeWriter = new QRCodeWriter();
	    BitMatrix bitMatrix = barcodeWriter.encode("One Text", BarcodeFormat.QR_CODE, 200, 200);
     
        BufferedImage originalImage = MatrixToImageWriter.toBufferedImage(bitMatrix);

        ByteArrayOutputStream baos = new ByteArrayOutputStream();
        ImageIO.write( originalImage, "jpg", baos );
        baos.flush();
        byte[] imageInByte = baos.toByteArray();
        baos.close();

        return Base64.getEncoder().encodeToString(imageInByte);
    }
```

The codes can be found: [SpringBoot](https://github.com/fagnercandido/qrcodewithspringboot) and [Quarkus](https://github.com/fagnercandido/qrcodewithquarkus)

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
