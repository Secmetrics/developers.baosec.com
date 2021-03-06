---
title: /registerURL
position: 1.1
type: post
description: Generate an U2F register URL
right_code: |
  ~~~ json
  {
    "code": 200,
    "message": "https://api.baosec.com/fido/u2f/v1/startRegistration?username=example-user&returnUrl=https://example.com/profile&challenge=d39ea54d7a127294033f6d9ff43e5f3d1f6ded3194bc7cda70acb04d5601872c&signature=fb5dbff9c91d0c7f20b661e076f2a91fdf30512694ffbfef7c5fd056ad569739"
  }
  ~~~
  {: title="Response" }

  ~~~ json
  {
    "code": 400,
    "message": "Bad URL format"
  }
  ~~~
  {: title="Error" }
---
username
: The username that already logged in your application

returnUrl
: The return URL after successful registered an U2F Security Key

Generate an U2F register URL with the given username and return URL then redirecting to it with your application.
{: .success }

The username must be unique in your application such as an email address.
{: .info }
