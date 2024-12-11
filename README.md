### **Chef-Restaurant App README**

# Chef-Restaurant App

The Chef-Restaurant app is a web application showcasing a variety of food items, allowing users to browse, filter, and search for meals based on their preferences. It consists of a React-based frontend and a Node.js backend, both deployed using Vercel.

---

## **Features**
- View a selection of food items with details like name, description, price, and image.
- Filter food items by categories: Breakfast, Lunch, Dinner.
- Search food items by name.
- Dynamic image loading from the backend.

---

## **Tech Stack**
- **Frontend**: React, Styled-Components
- **Backend**: Node.js, Express
- **Deployment**: Vercel

---

## **How to Run Locally**

### **1. Clone the Repository**

```bash
git clone https://github.com/Prakashkumar88/Chef-Restaurant.git
cd Chef-Restaurant
```

### **2. Install Backend Dependencies**

Navigate to the `server` folder and install dependencies:

```bash
cd server
npm install
```

### **3. Run the Backend**

To run the backend locally:

```bash
npm start
```

The backend server will be available at `http://localhost:9000` and serves static images from the `server/public/images` folder.

### **4. Install Frontend Dependencies**

Navigate to the `app` folder and install dependencies:

```bash
cd ../app
npm install
```

### **5. Run the Frontend**

To run the frontend locally:

```bash
npm run dev
```

The frontend will be available at `http://localhost:3000`.

---

## **Deployment**

### **Frontend**  
Deployed using Vercel. Visit:  
[Frontend Deployment](https://chef-restaurant-frontend.vercel.app)

### **Backend**  
Deployed using Vercel. Visit:  
[Backend Deployment](https://chef-restaurant-server.vercel.app)

---

## **Directory Structure**

```
Chef-Restaurant/
│
├── server/
│   ├── public/
│   │   └── images/       # Image files (e.g., egg.png, ramen.png, etc.)
│   ├── src/
│   │   └── index.ts      # Backend server code
│   └── package.json      # Backend dependencies
│
├── app/
│   ├── public/
│   │   └── logo.webp     # App logo
│   ├── src/
│   │   └── App.js        # Frontend React code
│   └── package.json      # Frontend dependencies
│
├── .gitignore            # Git ignore file
├── vercel.json           # Vercel configuration
└── README.md             # Project documentation
```

---

## **Adding Images**

1. **Backend Images**:
   - Place images in the `server/public/images` directory.
   - The backend serves them at `/images`. Example:
     ```
     https://chef-restaurant-server.vercel.app/images/egg.png
     ```

2. **Frontend Images**:
   - Use `BASE_URL` to dynamically load images:
     ```javascript
     <img src={`${BASE_URL}${image}`} alt="Food Item" />
     ```
   - Set `BASE_URL` to the deployed backend URL: `https://chef-restaurant-server.vercel.app`.

---

## **Troubleshooting**

### **Images Not Loading**
- Ensure the images are deployed in the `server/public/images` directory.
- Verify the image URL by accessing it directly in the browser, e.g., `https://chef-restaurant-server.vercel.app/images/egg.png`.

### **Unable to Fetch Data**
- Check the backend server status. Ensure it is running and accessible.
- Verify the API endpoint URL in the frontend.

---

## **Contributing**

We welcome contributions to improve the Chef-Restaurant app. To contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`.
3. Make your changes and commit: `git commit -m 'Add new feature'`.
4. Push to your fork: `git push origin feature-name`.
5. Submit a pull request.

---

## **License**

This project is licensed under the MIT License. Feel free to use and modify it as needed.

---

Let me know if additional details are required or if you’d like further adjustments!
