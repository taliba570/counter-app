
# CounterApp

CounterApp is a React Native mobile application that tracks multiple counters. Each counter has a title and a value that can be incremented or decremented. The application persists data using a NestJS backend with MongoDB, ensuring that counter states are maintained even after the app is closed.

## Features

- Create and manage multiple counters.
- Increment and decrement counter values.
- Persistent storage using a NestJS backend and MongoDB.
- Modern React Native UI with navigation.

## Tech Stack

- **Frontend**: React Native
- **Backend**: NestJS
- **Database**: MongoDB

---

## Getting Started

### Prerequisites

1. **Node.js** (version 12 or higher)
2. **npm** or **yarn**
3. **MongoDB** server running locally or a MongoDB Atlas account
4. **React Native CLI** (for running the mobile app)

### Backend Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/CounterApp.git
   cd CounterApp/backend
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure MongoDB:**
   - Create a `.env` file in the `backend` directory with the following content:
     ```env
     MONGO_URI=mongodb://localhost/nest-counter # Update this with your MongoDB connection string
     ```

4. **Run the backend server:**
   ```bash
   npm run start
   ```
   - The server will start on `http://localhost:3000`

5. **API Endpoints:**
   - `POST /counter`: Create a new counter with a title.
   - `GET /counter`: Get all counters.
   - `GET /counter/:id`: Get a specific counter by ID.
   - `PUT /counter/increment/:id`: Increment the counter by 1.
   - `PUT /counter/decrement/:id`: Decrement the counter by 1.
   - `DELETE /counter/:id`: Delete a counter by ID.

### Frontend Setup

1. **Navigate to the React Native project directory:**
   ```bash
   cd CounterApp/frontend
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run the application:**
   - For Android:
     ```bash
     npx react-native run-android
     ```
   - For iOS:
     ```bash
     npx react-native run-ios
     ```

4. **Configure the backend URL:**
   - Update the base URL for API calls in the frontend code to match your backend server (usually in `src/api.js` or directly in the screens).

5. **App Structure:**
   - **`App.js`**: Main entry point with navigation setup.
   - **`src/screens/HomeScreen.js`**: Displays the list of counters and options to navigate or add new counters.
   - **`src/screens/CounterScreen.js`**: Manages individual counter details and actions.

### Folder Structure

```
CounterApp/
│
├── backend/                 # NestJS backend
│   ├── src/
│   ├── .env
│   ├── package.json
│   └── ...
│
└── frontend/                # React Native frontend
    ├── src/
    │   ├── screens/
    │   │   ├── HomeScreen.js
    │   │   ├── CounterScreen.js
    │   │   └── ...
    │   └── ...
    ├── App.js
    ├── package.json
    └── ...
```

---

## Development Tips

- **Backend**: Use `npm run start:dev` to run the server in watch mode for live-reloading during development.
- **Frontend**: Use React Native's development tools like the Debugger, Reload, and Hot Reloading.
- **API Testing**: Use tools like Postman or Insomnia to test backend APIs.
- **Database**: Manage your MongoDB data using MongoDB Compass or similar tools.

## Contributions

Feel free to open issues, contribute with pull requests, or suggest features for this project. Follow standard practices for code style and commit messages.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For any questions or support, please contact [Talib Allauddin](mailto:taliballauddin@gmail.com).

---

Happy Coding! 🎉

---

## Additional Notes

- Ensure you have all the necessary development environment setups, like Android Studio or Xcode, for running React Native apps.
- Backend and frontend servers should be running simultaneously to fully test the app.
- If you encounter any issues, refer to the documentation of React Native, NestJS, and MongoDB for troubleshooting.

---

## Resources

- [React Native Documentation](https://reactnative.dev/docs/getting-started)
- [NestJS Documentation](https://docs.nestjs.com/)
- [MongoDB Documentation](https://docs.mongodb.com/)

This README provides a comprehensive guide to get you started with the CounterApp project. For any further questions or detailed guidance, consult the respective documentation or reach out to the community for support.