ClinicPlus - Your Digital Healthcare Companion:
ClinicPlus is a full-stack web application built with the MERN stack (MongoDB, Express.js, React-ready frontend, Node.js) that connects patients with healthcare providers.  

 Prerequisites:
Before you dive in, make sure you have these installed:
- **Node.js** (version 14 or higher)
- **MongoDB Atlas account** (or local MongoDB)
- **Gmail account** (for password reset emails)
- **Git** (for version control)

Installation:

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ClinicPlus.git
   cd ClinicPlus
   ```

2. **Install server dependencies**
   ```bash
   cd server
   npm install
   ```

3. **Set up environment variables**
   ```bash
   node setup-env.js
   ```
   
   Then edit the `.env` file with your actual credentials:
   ```env
   MONGO_URI=your-mongodb-atlas-connection-string
   JWT_SECRET=your-super-secret-jwt-key
   EMAIL_USER=your-gmail@gmail.com
   EMAIL_PASS=your-16-character-app-password
   ```

4. **Start the server**
   ```bash
   npm start
   ```

5. **Open the frontend**
   - Navigate to the `client` folder
   - Open `index.html` in your browser
   - Or serve it using a local server

Configuration Guide:

Email Setup (Required for Password Reset)

-To enable the "Forgot Password" feature, you need to configure Gmail:

1. **Enable 2-Step Verification** on your Google Account
2. **Generate an App Password**:
   - Go to Google Account → Security → 2-Step Verification → App passwords
   - Select "Mail" and "Other"
   - Copy the 16-character password
3. **Update your .env file** with the credentials

-Database Setup

1. **MongoDB Atlas** (Recommended):
   - Create a free cluster at [mongodb.com](https://mongodb.com)
   - Get your connection string
   - Update `MONGO_URI` in your `.env` file

2. **Local MongoDB** (Alternative):
   - Install MongoDB locally
   - Use `mongodb://localhost:27017/clinicplus`

How to Use:

-For Patients

1. **Register/Login**: Create an account or sign in
2. **Browse Clinics**: View available healthcare facilities
3. **Find Doctors**: Search by specialization and clinic
4. **Book Appointments**: Choose your preferred time slot
5. **Manage Bookings**: View, cancel, or reschedule appointments

-For Doctors

1. **Complete Profile**: Add specialization, experience, and contact info
2. **Set Availability**: Define your working hours
3. **View Appointments**: See your patient schedule
4. **Manage Information**: Update your profile and clinic details

-Forgot Password?

1. Click "Forgot Password?" on the login page
2. Enter your registered email address
3. Check your email for the 6-digit OTP
4. Enter the OTP and set a new password
5. Done! 
