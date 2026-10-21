# Govt Primary School Ahloo — Online School Management System

## Important
This is a Firebase-based starter project. It is not live until you configure Firebase and deploy it to a hosting provider.

## 1. Configure Firebase
1. Open the Firebase Console and create a project.
2. Enable **Authentication > Email/Password**.
3. Create a **Cloud Firestore** database.
4. Register a Web App and copy its configuration into `firebase-config.js`.
5. The school ID is configured as `35210449`. Keep it consistent with the Firestore rules and school user records.

## 2. Create the first administrator
1. In Firebase Authentication, add the administrator’s email and password.
2. Copy the user UID.
3. In Firestore, create `schools/35210449/users/USER_UID` (replace `USER_UID` with the actual UID).
4. Add fields: `name` (string), `email` (string), `role` (string: `admin`), and `active` (boolean: `true`).

## 3. Deploy
Serve the project over HTTP/HTTPS; do not open `index.html` directly with a `file://` URL. You can use Firebase Hosting or another static hosting provider. Install Firebase CLI, run `firebase login`, then from this folder run `firebase use --add` and `firebase deploy`. Review `firebase.json` before deployment.

## Included modules
Dashboard, students, staff, attendance, salary estimates, expenses, exams/results, user roles, and JSON backup/restore. The interface is in English and uses the school name **Govt Primary School Ahloo**.

## Important limitations
- The old standalone app stores data in the browser on a single device. This online app uses Firebase and does not automatically import old local data.
- Salary deductions use a simplified 30-day estimate and should be checked against your school’s official payroll policy.
- The Daily Attendance Register from the standalone app remains a separate local module; its school name and school code defaults have been updated, but it is not yet integrated into the Firebase online app.
- Test permissions and backup/restore with sample data before using real school records.
