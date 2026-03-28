# wanderlust 🌍✨

Welcome to **Wanderlust**, a web application designed to help you discover and manage unique accommodations and travel experiences around the world. Whether you're looking for a cozy beachfront cottage or a remote mountain cabin, Wanderlust aims to be your go-to platform for finding your next great adventure.

## 🌟 Key Features & Benefits

*   **Explore Diverse Listings**: Browse through a wide array of properties with detailed descriptions, images, and pricing.
*   **Create New Listings**: Easily add your own unique accommodations for others to discover.
*   **Manage Your Properties**: Edit or delete your existing listings with intuitive controls.
*   **Detailed Views**: Get comprehensive information about each property, including location and specific details.
*   **Robust Backend**: Built with Node.js and Express, ensuring a performant and scalable application.
*   **Persistent Data Storage**: Utilizes MongoDB to reliably store all listing information.
*   **Pre-populated Data**: Comes with sample listings to get you started immediately.

## 🛠️ Prerequisites & Dependencies

Before you begin, ensure you have the following installed on your system:

*   **Node.js**: A JavaScript runtime environment. (LTS recommended)
*   **npm** (Node Package Manager): Comes bundled with Node.js.
*   **MongoDB**: A NoSQL database. Ensure it's installed and running locally.

The project also uses the following core technologies and libraries:

*   **JavaScript**: The primary programming language.
*   **Node.js**: Server-side runtime.
*   **Express.js**: Web framework for Node.js.
*   **Mongoose**: MongoDB object modeling tool.
*   **EJS (Embedded JavaScript)**: Templating engine for dynamic HTML.
*   **Method-Override**: Middleware to enable `PUT` and `DELETE` HTTP verbs.

## 🚀 Installation & Setup Instructions

Follow these steps to get Wanderlust up and running on your local machine:

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/sourya-guha/wanderlust.git
    cd wanderlust
    ```

2.  **Install Dependencies**:
    Navigate to the project root and install all required Node.js packages:
    ```bash
    npm install
    ```

3.  **Start MongoDB Server**:
    Ensure your local MongoDB instance is running. If not, start it. The connection URL defaults to `mongodb://127.0.0.1:27017/wanderlust`.

4.  **Initialize Database with Sample Data**:
    To populate your database with initial listings, run the initialization script:
    ```bash
    node init/index.js
    ```
    You should see a message `data was initialized`.

5.  **Start the Application Server**:
    Finally, start the Express application:
    ```bash
    node app.js
    ```
    You should see `connected to DB` in your console, followed by `app is listening on port 8080` (or whichever port it's configured to run on, typically 3000 or 8080).

6.  **Access the Application**:
    Open your web browser and navigate to `http://localhost:8080` (or the port specified in your console) to view the application.

## 💡 Usage Examples

Once the application is running, you can interact with it via your web browser:

*   **View All Listings**:
    Navigate to the home page (`/`) or `http://localhost:8080/listings` to see all available properties.
    ![All Listings Page](https://via.placeholder.com/800x400?text=Wanderlust+All+Listings)

*   **View a Specific Listing**:
    Click on any listing from the main page to view its detailed information. The URL will look like `http://localhost:8080/listings/:id` (e.g., `http://localhost:8080/listings/60c72b2f9c1d4a001c8e4d3c`).
    ![Single Listing Page](https://via.placeholder.com/800x400?text=Wanderlust+Single+Listing)

*   **Add a New Listing**:
    Access the "Create New Listing" form via `http://localhost:8080/listings/new`. Fill in the details and submit.
    ![New Listing Form](https://via.placeholder.com/800x400?text=Wanderlust+New+Listing+Form)

*   **Edit a Listing**:
    On a specific listing's detail page, there will be an "Edit" button that takes you to `http://localhost:8080/listings/:id/edit`. Modify the details and update.
    ![Edit Listing Form](https://via.placeholder.com/800x400?text=Wanderlust+Edit+Listing+Form)

*   **Delete a Listing**:
    From a specific listing's detail page, there will be a "Delete" option to remove the listing permanently.

## ⚙️ Configuration Options

The primary configuration for the database connection is managed within `app.js` and `init/index.js`.

*   **MongoDB Connection URL**:
    The `MONGO_URL` variable defines the connection string for your MongoDB instance.
    ```javascript
    // In app.js and init/index.js
    const MONGO_URL = "mongodb://127.0.0.1:27017/wanderlust";
    ```
    You can modify this value if your MongoDB server is running on a different port, host, or if you're connecting to a remote database (e.g., MongoDB Atlas). For production environments, it's recommended to use environment variables (e.g., `process.env.MONGO_URL`) to manage such sensitive information.

## 🤝 Contributing Guidelines

Contributions are always welcome! If you'd like to contribute to Wanderlust, please follow these steps:

1.  **Fork** the repository on GitHub.
2.  **Clone** your forked repository to your local machine.
    ```bash
    git clone https://github.com/YourUsername/wanderlust.git
    ```
3.  **Create a new branch** for your feature or bug fix.
    ```bash
    git checkout -b feature/your-feature-name
    ```
4.  **Make your changes**, ensuring they adhere to the existing code style.
5.  **Commit your changes** with a clear and descriptive commit message.
    ```bash
    git commit -m "feat: Add new feature for user profiles"
    ```
6.  **Push your changes** to your forked repository.
    ```bash
    git push origin feature/your-feature-name
    ```
7.  **Open a Pull Request** from your forked repository to the `main` branch of the original repository. Describe your changes in detail.

## 📄 License Information

This project currently does not have a specified license. Please contact the owner, sourya-guha, for licensing details or before using this project for commercial purposes.

## 🙏 Acknowledgments

*   Special thanks to [Unsplash](https://unsplash.com/) for providing beautiful, high-quality images used as placeholders in the sample data.
