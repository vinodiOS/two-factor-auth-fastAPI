# Two Factor Authentication using FastAPI

This repository uses [FastAPI](https://fastapi.tiangolo.com) for creating webapp and [PyOTP](https://pypi.org/project/pyotp/) Python library is used for generating and verifying one-time passwords.

## Installation

```sh
git clone https://github.com/vinodiOS/two-factor-auth-FastAPI.git
cd two-factor-auth-FastAPI
virtualenv venv 
source env/bin/activate 
pip install -r requirements.txt
uvicorn main:app --reload
```

## Steps for setting up Two Factor Authentication

Follow next steps for setting up user account and generate TOTP using Authenticator app.

## Signup
Enter the following path to create new user.
```sh
http://127.0.0.1:8000/signup/
```
![signup](https://user-images.githubusercontent.com/30258541/161042216-e2aa8a50-4dd3-4629-98d6-b1152705459d.png)

## QR Code Generation
After entering appropriate details new user would be created and page will be navigated to QR Code.

![qrcode_scan](https://user-images.githubusercontent.com/30258541/161043010-f698cb41-317a-4b61-801f-ceeb1c5674c8.png)

## Authenticator app setup

Use [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en_IN&gl=US) or [Microsoft Authenticator](https://play.google.com/store/apps/details?id=com.azure.authenticator&hl=en_IN&gl=US) or any other Authenticator app to scan QR code and generate TOTP.

![otp_screenshot](https://user-images.githubusercontent.com/30258541/161052537-ad536b1e-8c67-4fa8-88fe-31ab7ebb5b12.png)

## Login
Follow this path to login 
```sh
http://127.0.0.1:8000/login/
```

Enter user credentials along with 6 digit TOTP generated by Authenticator app.

![login](https://user-images.githubusercontent.com/30258541/161044503-d2497b0b-ab8a-4e4c-a50b-f2077010ea74.png)

And, welcome to your website. You have securely logged into your account.

![welcome](https://user-images.githubusercontent.com/30258541/161050065-aa4ece5f-2975-4b1f-8404-26d96db670f3.png)

Please star ✨ repository if you like it. Thank you!
