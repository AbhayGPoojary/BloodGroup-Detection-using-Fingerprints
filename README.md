# 🩸 Blood Group Prediction Web App using Flask & PyTorch

This is a web application that predicts a person's **blood group** based on an uploaded image using a **Convolutional Neural Network (CNN)** model trained in **PyTorch**. The app includes **user authentication**, image processing, and a web interface powered by **Flask**.

---

## 🚀 Features

- 🔐 User registration, login, profile update & logout
- 🧠 Blood group prediction using a pre-trained CNN model
- 📸 Image upload and preprocessing
- 📊 Accuracy chart visualization page
- 👨‍👩‍👧‍👦 Team page and about section
- 🔒 Passwords securely stored using hashing
- 🗃️ SQLite3 database for user data
- 📁 Image uploads stored in `static/uploads/`

---

## 🧰 Tech Stack

- **Backend**: Python, Flask
- **Frontend**: HTML, CSS, Jinja2
- **Model**: PyTorch (CNN)
- **Database**: SQLite
- **Others**: Werkzeug (for password hashing & secure file handling), Pillow (image loading)

---

## 🧠 Model Description

### Model Name: `SimpleCNN`


<!-- - **Architecture**:
  - `Conv2d(1, 32, kernel_size=3)`
  - `ReLU()`
  - `MaxPool2d(2, 2)`
  - `Linear(32*63*63 → 8)` — where 8 is the number of blood groups -->

### Output Labels:
```
['A+', 'A-', 'AB+', 'AB-', 'B+', 'B-', 'O+', 'O-']
```
<!-- 
- **Model File**: `new_model_testing.pkl`
- **Inference Device**: CPU -->

---

## 📁 Project Folder Structure

```
BloodGroupCNN/
│
├── Code/
│   ├── app.py                  # Main Flask application
│   ├── new_model_testing.pkl   # Trained PyTorch model
│   ├── templates/              # HTML templates
│   │   ├── index.html
│   │   ├── login.html
│   │   ├── signup.html
│   │   ├── result.html
│   │   ├── home.html
│   │   ├── chart.html
│   │   ├── about.html
│   │   ├── team.html
│   │   └── profile.html
│   ├── static/
│   │   └── uploads/            # Uploaded images stored here
│
├── users.db                    # SQLite database (auto-created)
├── requirements.txt            # Python dependencies
└── README.md                   # This file
```

---

## ⚙️ How to Run This Project Locally

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/BloodGroupCNN.git
cd BloodGroupCNN/Code
```

### Step 2: Create and Activate Virtual Environment

```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

If `requirements.txt` is missing, install manually:

```bash
pip install flask torch torchvision pillow werkzeug
```

### Step 4: Start the Flask App

```bash
python app.py
```

Visit in browser: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## ✨ Pages & Routes

| Route | Description |
|-------|-------------|
| `/` | Landing page |
| `/signup` | User registration |
| `/login` | User login |
| `/logout` | Logout |
| `/home` | Dashboard after login |
| `/predict_blood_group` | Upload and predict blood group |
| `/profile` | User profile |
| `/about`, `/team`, `/Accurancy` | Additional pages |
| `/predict` | (POST only) Accepts image and returns prediction |

---

## ✅ Requirements

Make sure the following dependencies are included in your `requirements.txt`:

```txt
flask
torch
torchvision
pillow
werkzeug
```

<!-- 
## 🔐 Security Notes

- Passwords are stored using Werkzeug's secure hashing.
- File uploads are saved with `secure_filename()` to prevent path traversal.
- Sessions are used to manage login states securely with a `secret_key`.

---

## 📬 Example Prediction Flow

1. User signs up or logs in.
2. Navigates to `/predict_blood_group`
3. Uploads an image → Server processes and sends it through CNN model
4. Predicted blood group is displayed on the `result.html` page

--- -->

<!-- ## 🧠 To Train Your Own Model (Optional)

If you want to train your own model and generate `new_model_testing.pkl`, follow these general steps:

1. Collect and label images for 8 blood groups.
2. Build a PyTorch CNN (like `SimpleCNN`)
3. Train on grayscale images resized to 128x128.
4. Save the model using:
```python
torch.save(model.state_dict(), 'new_model_testing.pkl')
``` -->

---

## 👨‍💻 Contributors

- **Your Name** – Abhay G Poojary
- **Team Members** – Adish Poojary , Karthik Nayak , Kiran Divakar Salian


---
<!-- 
## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 📌 Contact

For any issues, reach out to: [your-email@example.com](mailto:your-email@example.com)

---

> ⭐ Star this repo if you found it useful! -->
