[server.js](https://github.com/user-attachments/files/26551057/server.js)
const express = require("express");
const cors = require("cors");

const app = express();
app.use(cors());

// dữ liệu giả (sau này sẽ là database)
const products = ["Áo", "Quần", "Giày"];

// API trả dữ liệu
app.get("/api/products", (req, res) => {
    res.json(products);
});

app.listen(3000, () => {
    console.log("Server chạy tại http://localhost:3000");
});
