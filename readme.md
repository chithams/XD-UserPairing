# Cross-Device User Pairing
This respository contains an extension of the [XD-MVC](https://github.com/mhusm/XD-MVC) cross-device framework which facilitates user-based device pairing.
We have included two applications demonstrating the usage of the framework.


* [Gallery](https://github.com/mhusm/XD-Gallery) is an existing photo sharing application developed by my supervisor,  [Maria Husmann](https://globis.ethz.ch/#!/person/maria-husmann/). Previously, device pairing
was handled by QR codes and URLs. We improved the user experience of device pairing by
utilizing our contacts-list Polymer element.
* Shared Booking is a cross-device hotel booking application.

## Installation
This project requires [node.js](nodejs.org) and [bower](bower.io). In a console, run the following commands in the root of the project.


1. `npm install`
2. `bower install`

## Starting the demo applications


1. `node gallery-p2p.js`
2. Point your browser to http://hostname:8082/galleryp2p.html or http://hostname:8082/sharedBooking.html
3. Log in with your Google account
4. Log in with the same account on another device for automatic pairing or connect with your available contacts

## Setup for using the framework
Developers can either directly use our JavaScript API or integrate the default Polymer UI components
into their application.

###Directly using the JavaScript API:
Add the following line after the XD-MVC imports in  the head section of the HTML file and then make API calls on the XD-MVC object.
```html
<script src="../bower_components/xdmvcclient/js/userpairing.js"></script>
```

###Using the Polymer UI elements:
Import the elements that you are going to use in the header.
```html
<link rel="import" href="elements/login-google.html">
<link rel="import" href="elements/contacts-list.html">
```
or
```html
<link rel="import" href="elements/login-google.html">
<link rel="import" href="elements/contacts-drawer.html">
```

Add the elements to the application's body.
When using the contacts-drawer element, the content of the application must be inserted between the contacts-drawer HTML tags.
```html
<body>
  ...
  <login-google></login-google>
  <contacts-list></contacts-list>
  ...
</body>
```
or

```html
<body>
  <contacts-drawer>
    <login-google></login-google>
    ...
    ...
  </contacts-drawer>
</body>
```

## About this Project
XD-UserPairing and the two demo applications were developed during my bachelor thesis at the [Globis Group at ETH Zürich](https://globis.ethz.ch) under the supervision of Prof. Dr. Moira C. Norrie and [Maria Husmann](https://globis.ethz.ch/#!/person/maria-husmann/).
