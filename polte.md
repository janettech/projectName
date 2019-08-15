### Polte's Register and Locate Device Getting Started Guide
#### This is to get you started with registering your device with Polte and track the location of your device.
Polte provides you with Swagger tool to try out Polte's Location Service APIs.

## 1.Claim the device
1. You should have a polte.io account. (Polte Admin will create an account for you).
2. Login and claim the UE- Bulk claim UE process.
3. **OR** call the API to claim /customer/{customerId}/userEquipment/claim. Go to the **Authorize Customer** section for help in authorizing yourself before using Polte API Reference library.

### Authorize Customer
Each request to the Polte API should include HTTP Authorization Header.
1. Go to [[https://polte.io/swagger/customer/](https://polte.io/swagger/customer/)]
2. Call the API /users/login with your polte.io credentials and Authorize with the Bearer token.
3. You are now authorized to call Polte APIs.

## 2.Register the device
1. To register, send (AT+POLTEREG?) command **OR**
 request the API call /ue/register/ at [https://polte.io/swagger/user-equipment/](https://polte.io/swagger/user-equipment/).
 2. Polte Cloud will return the mqtt tokens(username:password).


## 3.Locate the device
1. To locate, payload data is sent over (AT+POLTECOMPRESS) command. 
2. View the location on polte.io or track.polte.io
3. **OR** request the API call /ue/{ueToken}/locate to return location. Go to the **Authorize UE** section for help in authorizing your UE before using Polte UE API.
### Authorize UE
1. Go to [[https://polte.io/swagger/customer/](https://polte.io/swagger/customer/)].
2. Call the API /customer/{customerId}/apiTokens to create an API token.
3. Copy the API token.
4. Return to UE API- https://polte.io/swagger/user-equipment/ and authorize. (Format: Polte-API API-token).
5. You are now authorized to call UE APIs.



