# Car Analyzer Application

This is a React-based web application that allows users to upload an image of a car and analyze it using AI. The backend is built with Node.js and integrates with OpenAI to generate responses based on the uploaded image and the provided prompt.

## Features

- Upload a car image and get AI-generated information about the car.
- Use AI assistance to check details about the car in bullet points.
- Reset functionality to clear the form and start over.
- Uses OpenAI API to analyze the image and generate responses.

## Frontend

### Built With:
- React.js
- `useState` for managing state.
- Fetch API for making requests to the backend.
- CSS for styling.

### Main Components:
- **Upload Image**: Allows users to upload an image of the car.
- **AI Assistance**: Users can ask for information about the car (like brand, model, and type) in bullet points.
- **Reset Button**: Allows users to clear the image, reset the form, and start a new query.

## Backend

### Built With:
- Node.js
- Express
- CORS
- Multer for file uploads
- OpenAI API for AI integration
- dotenv for environment variable management

### Backend Functionality:
- **File Upload**: The backend allows users to upload images using Multer. The images are stored temporarily and processed to extract car information.
- **Image Analysis**: After uploading the image, the backend uses OpenAI's API to analyze the image and generate a response based on the user's request.
- **Endpoints**:
  - `POST /upload`: Uploads the image to the server.
  - `POST /ImageAnalyzer`: Analyzes the uploaded image using OpenAI.

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- React.js (v17 or higher)
- MongoDB (optional if you want to store data)

### Installation

1. Clone the repository:

   ```bash
   git clone <repo-url>
   cd <repo-directory>
   ```

2. Install dependencies for both frontend and backend:

   - **Frontend**:
     ```bash
     cd frontend
     npm install
     ```
     
   - **Backend**:
     ```bash
     cd ../backend
     npm install
     ```

3. Set up environment variables:
   
   Create a `.env` file in the `backend` directory with the following:

   ```
   OPENAI_API_KEY=your_openai_api_key
   PORT=8000
   ```

4. Start the backend server:

   ```bash
   cd backend
   npm start
   ```

5. Start the frontend development server:

   ```bash
   cd ../frontend
   npm start
   ```

6. Open `http://localhost:3000` in your browser to view the application.

## Usage

- Upload an image of a car.
- Click "Ask" to query information about the car.
- The AI will analyze the image and return details like brand, model, and type.
- If needed, you can click the "Reset" button to upload another image.

## API Documentation

- **`POST /upload`**: Upload an image.
  - Request Body: Image file (multipart/form-data).
  - Response: Confirms upload success or failure.

- **`POST /ImageAnalyzer`**: Analyze the uploaded image and return AI-generated information.
  - Request Body: 
    - `message`: A text query (e.g., "What is the brand, model, and type of the car?").
  - Response: AI-generated text response about the car.

## Example Query

1. Upload an image of a car.
2. Click "Ask" to analyze the car. For example:
   ```
   What is the brand, model, and type of the car in bullet points?
   ```
3. The AI will return something like:
   - Brand: Toyota
   - Model: Corolla
   - Type: Sedan

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any bugs or improvements.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
