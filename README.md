# MERN-Auth


<img width="1280" height="800" alt="Screenshot 2025-08-11 at 11 02 10 PM" src="https://github.com/user-attachments/assets/eb3bc58c-b442-4a6b-ab81-d3f6875b153f" />

1️⃣ Signup Page – Empty Form

The signup form where users can enter name, email, and password to create a new account.

Clean UI with placeholders and a Signup button.

On submission, backend hashes the password using bcrypt and generates a JWT token for the new user

<img width="1280" height="800" alt="Screenshot 2025-08-11 at 11 02 21 PM" src="https://github.com/user-attachments/assets/6c079e86-893e-4df2-a875-58a76c65be17" />

2️⃣ Signup Page – Name Entered

Name field has been filled (siriB).

Browser’s autocomplete suggestion shows previously used emails.

Once completed and submitted, the backend will return a JWT token to maintain authentication.

<img width="1280" height="800" alt="Screenshot 2025-08-11 at 11 02 29 PM" src="https://github.com/user-attachments/assets/62370910-9a42-40c4-b9a4-7550f25abe85" />

3️⃣ Signup Page – Filled Form

Name, email, and password fields are filled, ready to submit.

After submission, backend stores the hashed password in MongoDB Atlas and sends back a JWT token stored in the browser for session handling.



<img width="1280" height="800" alt="Screenshot 2025-08-11 at 11 02 43 PM" src="https://github.com/user-attachments/assets/a99f5280-fcbf-4a3f-b1c5-0e21c26fe55d" />

4️⃣ Login Page – Filled Form

Existing user (basuthkarsiri.2004@gmail.com) enters credentials.

Backend verifies the password using bcrypt and issues a new JWT token if credentials are valid.

Token is used to authenticate all further API requests without needing to log in again.




<img width="1280" height="800" alt="Screenshot 2025-08-11 at 11 02 48 PM" src="https://github.com/user-attachments/assets/0b7b4d5f-3207-4381-928c-2390bb25af82" />


5️⃣ Home Page – Authenticated

After login, the backend decodes the stored JWT token to confirm user identity.

Displays "Welcome siriB" and the success message: Successfully authenticated. Thank you for using our service.

The token ensures that even if the page is refreshed, the user remains logged in until the token expires or is removed (via logout).




<img width="1280" height="800" alt="Screenshot 2025-08-11 at 11 05 43 PM" src="https://github.com/user-attachments/assets/8111d2c6-9c63-43af-b2e8-8a497dbdf5a8" />

6️⃣ MongoDB Atlas – Users Collection

Shows stored user records inside the author → users collection.

Passwords are hashed with bcrypt — not stored as plain text.

JWT tokens are not stored in the database but sent to the client upon successful login/signup.

This ensures stateless authentication, where the server validates the token without storing session data.



