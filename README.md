# Laravel jUploader
A jQuery-File-Upload bundle for the Laravel Framework

## Requirements
* [Bootstraper Enhanced Bundle](https://github.com/Pasvaz/bootstrapper) OR [Bootstraper Bundle](https://github.com/patricktalmadge/bootstrapper/)

----
<a name='installation'></a>
## Installation

Type the following in your Terminal :

```bash
php artisan bundle:install juploader
```

Add the following to your `bundles.php` file :

```php
'juploader' => array('handles' => 'upload'),
```

Install Bootstrapper if you didn't already :

```bash
php artisan bundle:install bootstrapper
```

And finally publish the bundle assets :

```bash
php artisan bundle:publish
```

Visit http://127.0.0.1/upload and play with the demos in order to get used with jUploader

Alternatively you can download it directly from GitHub:
http://github.com/Pasvaz/laravel-juploader


----

<a name='usage'></a>
## Usage

### Assets

Load these Assets in order to make it working
```php
{{ Asset::container('bootstrapper')->styles() }}
{{ Asset::container('juploader')->styles() }}
{{ Asset::container('juploader-gallery')->styles() }}

{{ Asset::container('bootstrapper')->scripts() }}
{{ Asset::container('juploader')->scripts() }}
{{ Asset::container('juploader-gallery')->scripts() }}
/* The gallery is optional */
```

### Markup
Setup a multipart/form-data Form:
```php
<form id="fileupload" action="{{ URL::to_route('upload') }}" method="POST" enctype="multipart/form-data">
...
</form>
```
Create the ButtonBar:
```php
<form id="fileupload" action="{{ URL::to_route('upload') }}" method="POST" enctype="multipart/form-data">

{{Uploader\ButtonBar::create()}}

</form>
```

And finally display the templates:
```php
<form id="fileupload" action="{{ URL::to_route('upload') }}" method="POST" enctype="multipart/form-data">

{{Uploader\ButtonBar::create()}}

</form>

{{ Uploader\Templater::showAll() }}
```

----

# jQuery File Upload
## Demo
[jQuery-File-Upload](http://blueimp.github.com/jQuery-File-Upload/)

## Setup
[How to setup the plugin on your website](https://github.com/blueimp/jQuery-File-Upload/wiki/Setup)

## Features
* **Multiple file upload:**  
  Allows to select multiple files at once and upload them simultaneously.
* **Drag & Drop support:**  
  Allows to upload files by dragging them from your desktop or filemanager and dropping them on your browser window.
* **Upload progress bar:**  
  Shows a progress bar indicating the upload progress for individual files and for all uploads combined.
* **Cancelable uploads:**  
  Individual file uploads can be canceled to stop the upload progress.
* **Resumable uploads:**  
  Aborted uploads can be resumed with browsers supporting the Blob API.
* **Chunked uploads:**  
  Large files can be uploaded in smaller chunks with browsers supporting the Blob API.
* **Client-side image resizing:**  
  Images can be automatically resized on client-side with browsers supporting the required JS APIs.
* **Preview images:**  
  A preview of image files can be displayed before uploading with browsers supporting the required JS APIs.
* **No browser plugins (e.g. Adobe Flash) required:**  
  The implementation is based on open standards like HTML5 and JavaScript and requires no additional browser plugins.
* **Graceful fallback for legacy browsers:**  
  Uploads files via XMLHttpRequests if supported and uses iframes as fallback for legacy browsers.
* **HTML file upload form fallback:**  
  Allows progressive enhancement by using a standard HTML file upload form as widget element.
* **Cross-site file uploads:**  
  Supports uploading files to a different domain with cross-site XMLHttpRequests or iframe redirects.
* **Multiple plugin instances:**  
  Allows to use multiple plugin instances on the same webpage.
* **Customizable and extensible:**  
  Provides an API to set individual options and define callBack methods for various upload events.
* **Multipart and file contents stream uploads:**  
  Files can be uploaded as standard "multipart/form-data" or file contents stream (HTTP PUT file upload).
* **Compatible with any server-side application platform:**  
  Works with any server-side platform (PHP, Python, Ruby on Rails, Java, Node.js, Go etc.) that supports standard HTML form file uploads.

## License
Released under the [MIT license](http://www.opensource.org/licenses/MIT).
