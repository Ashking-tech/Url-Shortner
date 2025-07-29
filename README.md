# 🔗 URL Shortener

A simple URL shortener built using **Node.js**, **Express**, **MongoDB**, and **nanoid**.

---

## 🚀 Features

- Shorten any valid URL
- Store and retrieve short URLs from MongoDB
- Redirect to the original URL when short URL is accessed
- Track visit analytics (click count + timestamps)

---

## 🛠️ Tech Stack

- **Node.js**
- **Express.js**
- **MongoDB**
- **Mongoose**
- **nanoid** – for generating unique short IDs

---

## 📦 Installation

```bash
git clone https://github.com/your-username/url-shortener.git
cd url-shortener
npm install
````

---

## ⚙️ Setup

1. Make sure MongoDB is running on your machine (default: `mongodb://localhost:27017`)
2. Create a `.env` file (optional) or update the MongoDB URL directly in your code
3. Start the server:

```bash
node index.js
```

Server will start on `http://localhost:8001`

---

## 📌 API Endpoints

| Method | Route                     | Description                   |
| ------ | ------------------------- | ----------------------------- |
| POST   | `/url`                    | Create a short URL            |
| GET    | `/:shortId`               | Redirect to original long URL |
| GET    | `/url/analytics/:shortId` | Get analytics for a short URL |

---

## 🧪 Example Usage

### ▶️ POST `/url`

**Request Body:**

```json
{
  "url": "https://www.theodinproject.com/"
}
```

**Response:**

```json
{
  "shortId": "5BUukYIo"
}
```

---

### 🔁 GET `/:shortId`

**Example:**

```
GET http://localhost:8001/5BUukYIo
```

**Redirects to:**

```
https://www.theodinproject.com/
```

---

### 📊 GET `/url/analytics/:shortId`

Returns total clicks and visit timestamps.

---

## 📁 Folder Structure

```
.
├── index.js
├── models/
│   └── url.js
├── routes/
│   └── Urls.js
├── controllers/
│   └── url.js
└── .gitignore
```

---


---

## 🙌 Acknowledgements

* [nanoid](https://github.com/ai/nanoid)
* [Express.js](https://expressjs.com/)
* [MongoDB](https://www.mongodb.com/)




