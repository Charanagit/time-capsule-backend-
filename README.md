# Time Capsule - Flask Backend

🚀 **Time Capsule** is a social media platform where users can post normally or schedule posts for a future date. The post will only become visible at the scheduled time, either privately or publicly.

## Features
✅ Post content normally like any social media platform  
✅ Schedule posts for a future date  
✅ Posts remain private until the set date arrives  
✅ MongoDB used for storing posts and user data  
✅ Flask backend with REST API endpoints  

## Tech Stack
- **Backend:** Flask (Python)
- **Database:** MongoDB (NoSQL)
- **Frontend:** [Shailesh Doiphode's GitHub Repository](https://github.com/Shailesh8421/socialmedia-clone)

## Installation & Setup

### Prerequisites
- Python 3.x installed
- MongoDB installed and running (or use MongoDB Atlas)

### Clone the Repository
```bash
git clone https://github.com/your-username/time-capsule-backend.git
cd time-capsule-backend
```

### Create and Activate Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate     # On Windows
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Setup Environment Variables
Create a `.env` file in the root directory and add the following:
```
MONGO_URI=mongodb://localhost:27017/timecapsule
SECRET_KEY=your_secret_key
```
*Replace `MONGO_URI` with your MongoDB Atlas URI if using a cloud database.*

### Run the Application
```bash
python app.py
```
The backend will be available at `http://127.0.0.1:5000/`

## Sample API Endpoints
| Method | Endpoint                | Description                  |
|--------|------------------------|------------------------------|
| POST   | `/api/register`        | Register a new user         |
| POST   | `/api/login`           | User login                  |
| POST   | `/api/posts`           | Create a new post           |
| GET    | `/api/posts`           | Get all posts               |
| GET    | `/api/posts/{id}`      | Get a specific post         |
| DELETE | `/api/posts/{id}`      | Delete a post               |

## Database Structure (MongoDB)
Example of a **post document**:
```json
{
  "_id": "ObjectId('...')",
  "user_id": "ObjectId('...')",
  "content": "This is a future post!",
  "is_scheduled": true,
  "scheduled_date": "2025-06-01T12:00:00Z",
  "created_at": "2025-02-23T10:00:00Z"
}
```

## Future Improvements
- Implement Docker for easy deployment 🚀
- Add JWT authentication 🔑
- Improve API security & rate limiting 🔐
- Enhance UI with a more interactive frontend 🎨

## Credits
🔹 **Frontend Repository:** [Shailesh Doiphode](https://github.com/Shailesh8421/socialmedia-clone)  
🔹 **Backend Developed By:** Charana Munasinghe 

## Contributing
Feel free to fork this repository and contribute to the project. Pull requests are welcome!  

## License
This project is open-source and available under the MIT License.



