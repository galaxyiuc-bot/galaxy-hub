---
title: Galaxy FTP Upload
---
# File Upload via FTP

<div class="alert alert-success" role="alert">
The address of FTP server for Main Galaxy is `usegalaxy.org`. Use the same email and password as for Galaxy.
</div>

Uploading data directly from the browser can be unreliable and cumbersome.
Because of this the [Main](/src/main/index.md) Galaxy allows you to upload data via FTP.
FTP will allow you to monitor the upload status as well as resume interrupted transfers.
Compression types .gz/.gzip, .bz/.bzip, .bz2/.bzip2, and single-file .zip are also supported.

## Introduction

If you are completely new to FTP transfers you might benefit from reading a [wikihow](http://www.wikihow.com/Use-FTP) page about it.

To get started using FTP with Galaxy, you'll need to have registered a regular Galaxy account. Once registered, you can initiate an FTP connection in your preferred FTP
client. Please see the [comparison](https://en.wikipedia.org/wiki/Comparison_of_FTP_client_software) of available FTP clients.

## Upload from client

In this example I'm using FileZilla for MacOS. Point your client to the FTP server hostname provided in the upload modal window (`usegalaxy.org` for Galaxy Main).
![FTP client connection details](ftp-connect.png)

<div class="alert alert-warning" role="alert">
If you are having trouble connecting to the [Main](/src/main/index.md) server try enabling FTP with `passive` mode in your client. **If using Filezilla, you must use FTP in `passive` mode.** Connect using `FTP`, `FTPS`, or `FTP-TLS` as `SFTP` connections will be rejected.
</div>

In most clients, when a connection is made with `FTP` or `FTPS`, a pop-up server certificate authentication will need to be accepted.

<div class="embed-responsive embed-responsive-16by9">
<iframe class="embed-responsive-item" src="https://player.vimeo.com/video/222236679?portrait=0" webkitallowfullscreen mozallowfullscreen allowfullscreen> </iframe>
</div>

In this video, the changes for `FTPS` are explained along with how to configure `FTP` client settings and verfify the target server's certificate.

Below you can see my files copied to the destination on Galaxy's FTP server.
![files uploaded to Galaxy FTP server](ftp-files.png)

## Import to Galaxy

Files uploaded to the FTP server won't automatically be imported to your history -
rather, you will be presented with a list of the contents of your FTP directory
in the standard upload interface. Select the ones you want to import and hit Start.

![FTP files on the Upload File tool form](ftp-select.png)

<div class="alert alert-warning" role="alert">
Files not imported within 3 days will be cleaned up from the FTP site.
</div>

## Configure for your Galaxy

FTP upload can be configured in local installations of Galaxy, instructions to do
so can be found at [admin/config/upload-via-ftp](/src/admin/config/upload-via-ftp/index.md).
