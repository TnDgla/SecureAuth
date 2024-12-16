### **Project Overview: Multi-Factor Authentication (MFA) System**

**SecureAuth:** This project involves developing a robust multi-factor authentication system to secure user accounts, combining Node.js, Express, Passport.js, and Speakeasy. The MFA system requires users to authenticate using two steps: username-password authentication and time-based OTP validation through an authenticator app like Google Authenticator.

---

### **Mission and Objectives**

**Goal:**  
To build a complete two-factor authentication system that secures user accounts and enhances overall application security.

**Objectives:**  
1. Implement a local authentication system using Passport.js.  
2. Incorporate time-based OTP (TOTP) generation and verification using Speakeasy.  
3. Ensure secure storage and retrieval of user data with MongoDB.  
4. Create secure routes for login, logout, status checks, and MFA setup, verification, and reset.  
5. Provide middleware to protect routes with authentication checks.

---

### **Technology Stack**

#### **Backend**
1. **Node.js**  
   - **Why?**: Enables building scalable and fast server-side applications.  
   - **Use Cases**: Core runtime for backend logic and API handling.

2. **Express.js**  
   - **Why?**: Simplifies RESTful API creation with middleware support.  
   - **Use Cases**: Defining routes and middleware for authentication and MFA.

3. **Passport.js**  
   - **Why?**: Provides strategies for handling authentication, including local strategies.  
   - **Use Cases**: Handling user login and session management.

4. **Speakeasy**  
   - **Why?**: Generates and verifies time-based OTPs.  
   - **Use Cases**: MFA setup and verification.

5. **MongoDB (with Mongoose)**  
   - **Why?**: Flexible NoSQL database for storing user credentials and MFA configurations.  
   - **Use Cases**: Storing user details, hashed passwords, and MFA secrets.

6. **JWT and bcrypt**  
   - **Why?**: Used for token generation and secure password hashing.  
   - **Use Cases**: Session tokens for API authentication and secure password storage.

---

### **Workflow Overview**

1. **User Login**:  
   - Username and password authentication using Passport.js.
   - Establish session and provide JWT tokens for secure interactions.

2. **MFA Setup**:  
   - Generate secret keys and QR codes using Speakeasy.
   - Validate user tokens via authenticator apps.

3. **Route Protection**:  
   - Middleware checks for session authentication and MFA activation.

4. **Session Management**:  
   - Serialize and deserialize users for session persistence.

---

### **System Architecture**

- **Routes**:  
  - **Auth Routes**: Login, logout, status checks.  
  - **MFA Routes**: Setup, verify, reset.  

- **Controllers**:  
  - Logic for handling user registration, login, MFA setup, token verification, and reset.

- **Middleware**:  
  - Authentication checks and session management.
  
![Screenshot (244)](https://github.com/user-attachments/assets/637e66c4-9d81-4831-bbf0-f63dfdf0cd56)
![Screenshot (245)](https://github.com/user-attachments/assets/5f772945-d096-4cf3-aefd-0a187d25105f)
![Screenshot (246)](https://github.com/user-attachments/assets/22b6a047-7acc-42ca-a857-fd4e816ebbca)

---

### **Project Structure for Feature Implementation**
- This project is structured to ensure a systematic and incremental development process. Each week builds upon the previous deliverables, enabling a smooth transition from basic to advanced functionalities.

**NOTE:** Participants are encouraged to customize the design and functionality to make the application unique.

---

### **Week-by-Week Learning Plan**

#### **Week 1: Project Setup and User Authentication**
- **Tasks**:
  1. Set up Node.js and initialize the project with npm.
     - **Reading**: [Node.js Documentation](https://nodejs.org/en/docs/)  
     - **Video**: [Node.js Basics](https://www.youtube.com/watch?v=TlB_eWDSMt4)
  2. Configure MongoDB and set up a connection.
     - **Reading**: [MongoDB Atlas Guide](https://www.mongodb.com/docs/atlas/getting-started/)  
     - **Video**: [MongoDB Atlas Walkthrough](https://www.youtube.com/watch?v=J6mDkcqU_ZE&t=30s)
  3. Create user schema with Mongoose for storing user details.
     - **Reading**: [Mongoose Guide](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/mongoose)  
     - **Video**: [Mongoose Walkthrough](https://www.youtube.com/watch?v=DZBGEVgL2eE&t=30s)

- **Deliverables**:
  - MongoDB connection and functional user schema.

---

#### **Week 2: Passport.js Integration**
- **Tasks**:
  1. Configure Passport.js for local authentication.
     - **Reading**: [Passport.js Documentation](http://www.passportjs.org/docs/)  
     - **Video**: [Passport.js Setup](https://www.youtube.com/watch?v=6FOq4cUdH8k)
  2. Implement registration and login logic.
     - **Reading**: [bcrypt.js Guide](https://www.npmjs.com/package/bcrypt)  
     - **Video**: [Authentication Flow](https://www.youtube.com/watch?v=USaB1adUHM0)

- **Deliverables**:
  - User registration and login functionality with Passport.js.

---

#### **Week 3: Session Management**
- **Tasks**:
  1. Serialize and deserialize users for session persistence.
     - **Reading**: [Express Sessions](https://www.npmjs.com/package/express-session)  
     - **Video**: [Session Management](https://www.youtube.com/watch?v=OH6Z0dJ_Huk)
  2. Implement middleware for route protection.

- **Deliverables**:
  - Secure route access with session management.

---

#### **Week 4: Multi-Factor Authentication**
- **Tasks**:
  1. Integrate Speakeasy for generating MFA secrets and tokens.
     - **Reading**: [Speakeasy Guide](https://www.npmjs.com/package/speakeasy)  
     - **Video**: [MFA Implementation](https://www.youtube.com/watch?v=igRUIfbihPQ)
  2. Create routes for MFA setup, token verification, and reset.
  3. Generate QR codes for user scanning.

- **Deliverables**:
  - Fully functional MFA with token verification.

---

#### **Week 5: Testing and Deployment**
- **Tasks**:
  1. Test API endpoints using Postman.
     - **Reading**: [Postman API Guide](https://learning.postman.com/docs/getting-started/introduction/)  
     - **Video**: [Postman Basics](https://www.youtube.com/watch?v=HvvE4BYghJ8)
  2. Deploy the application to Heroku or AWS.
     - **Reading**: [Heroku Deployment Guide](https://devcenter.heroku.com/articles/getting-started-with-nodejs)  
     - **Video**: [Heroku Deployment](https://www.youtube.com/watch?v=Q9foh9XTglE)

- **Deliverables**:
  - Deployed MFA system.

---

### **Screenshots for Reference**
- **MFA QR Code Generation**  
  ![QR Code](![image](https://github.com/user-attachments/assets/5fde4ef7-6c4a-4ae3-a50a-ee9c03db672a)
- **Login Page**  
  ![Login Page](![image](https://github.com/user-attachments/assets/1e6a1265-3a17-4688-b20f-49f0aa17da37)
- **Token Verification**  
  ![Token Verification](![image](https://github.com/user-attachments/assets/a05db9a0-439c-4bc8-82f9-272b1d5260ef)
---

## **References:**
1. [Node.js Documentation](https://nodejs.org/en/docs/)
2. [Passport.js Documentation](http://www.passportjs.org/docs/)
3. [Speakeasy Guide](https://www.npmjs.com/package/speakeasy)
4. [Express Sessions](https://www.npmjs.com/package/express-session)
5. https://www.youtube.com/watch?v=V2ctvKuI9hg

