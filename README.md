<!DOCTYPE html>
<html>
<head>
    <title>Page Title</title>
</head>
    <body>
   # Shekhar-Zone-b
Hii bhai  welcome 
### फाइल स्ट्रक्चर:
1. `index.html` (होमपेज)
2. `upload.html` (अपलोड पेज)
3. `products.html` (प्रोडक्ट्स पेज)
4. `styles.css` (CSS फाइल)
5. `script.js` (JavaScript फाइल)

### कोड (कॉपी-पेस्ट करके फाइलें बनाएं):

#### 1. index.html
```html
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shekhar Zone - कुछ भी बेचो, ग्राहक सीधे WhatsApp पर!</title>
    <meta name="description" content="Shekhar Zone: Buy and sell anything like mobiles, clothes, shoes, electronics. Upload your items and connect via WhatsApp.">
    <meta name="keywords" content="Shekhar Zone, buy sell, mobiles, clothes, shoes, electronics, WhatsApp marketplace">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Shekhar Zone</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="products.html">Products</a>
            <a href="upload.html">Upload Item</a>
        </nav>
    </header>
    <main>
        <section class="hero">
            <h2>Shekhar Zone — कुछ भी बेचो, ग्राहक सीधे WhatsApp पर!</h2>
            <p>Upload your products and let customers message you directly on WhatsApp.</p>
            <a href="upload.html" class="btn upload-btn">Upload Your Item</a>
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Shekhar Zone. All rights reserved.</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
```

#### 2. upload.html
```html
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Upload Item - Shekhar Zone</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Shekhar Zone</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="products.html">Products</a>
            <a href="upload.html">Upload Item</a>
        </nav>
    </header>
    <main>
        <section class="upload-form">
            <h2>Upload Your Item</h2>
            <form id="uploadForm">
                <label for="itemName">Item Name (आइटम का नाम):</label>
                <input type="text" id="itemName" required>

                <label for="itemPrice">Price (कीमत):</label>
                <input type="number" id="itemPrice" required>

                <label for="itemDetails">Details (विवरण):</label>
                <textarea id="itemDetails" required></textarea>

                <label for="itemImage">Image (फोटो):</label>
                <input type="file" id="itemImage" accept="image/*" required>

                <button type="submit" class="btn">Upload</button>
            </form>
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Shekhar Zone. All rights reserved.</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
```

#### 3. products.html
```html
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Products - Shekhar Zone</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Shekhar Zone</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="products.html">Products</a>
            <a href="upload.html">Upload Item</a>
        </nav>
    </header>
    <main>
        <section class="products">
            <h2>Available Products</h2>
            <div id="productList"></div>
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Shekhar Zone. All rights reserved.</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
```

#### 4. styles.css
```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: lightblue;
    color: #333;
}

header {
    background-color: white;
    padding: 1rem;
    text-align: center;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

nav a {
    margin: 0 1rem;
    text-decoration: none;
    color: #007bff;
}

.hero {
    text-align: center;
    padding: 2rem;
    background-color: white;
    margin: 1rem;
    border-radius: 8px;
}

.btn {
    background-color: #25d366; /* WhatsApp green */
    color: white;
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    text-decoration: none;
    display: inline-block;
}

.upload-btn {
    margin-top: 1rem;
}

.upload-form {
    max-width: 600px;
    margin: 2rem auto;
    padding: 1rem;
    background-color: white;
    border-radius: 8px;
}

form label {
    display: block;
    margin-top: 1rem;
}

form input, form textarea {
    width: 100%;
    padding: 0.5rem;
    margin-top: 0.5rem;
}

.products {
    padding: 2rem;
}

.product-item {
    background-color: white;
    margin: 1rem 0;
    padding: 1rem;
    border-radius: 8px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.product-item img {
    max-width: 200px;
    height: auto;
}

footer {
    text-align: center;
    padding: 1rem;
    background-color: white;
}

/* Mobile responsive */
@media (max-width: 768px) {
    .hero h2 {
        font-size: 1.5rem;
    }
    .product-item {
        flex-direction: column;
    }
}
```

#### 5. script.js
```javascript
// Load products from localStorage
function loadProducts() {
    const products = JSON.parse(localStorage.getItem('products')) || [];
    const productList = document.getElementById('productList');
    if (productList) {
        productList.innerHTML = '';
        products.forEach(product => {
            const itemDiv = document.createElement('div');
            itemDiv.className = 'product-item';
            itemDiv.innerHTML = `
                <img src="${product.image}" alt="${product.name}">
                <h3>${product.name}</h3>
                <p>Price: ₹${product.price}</p>
                <p>${product.details}</p>
                <a href="https://wa.me/919236682603?text=${encodeURIComponent(`नमस्ते, मैंने आपका आइटम ${product.name} Shekhar Zone पर देखा है। क्या अभी उपलब्ध है?`)}" class="btn">Message Seller on WhatsApp</a>
            `;
            productList.appendChild(itemDiv);
        });
    }
}

// Handle upload form
const uploadForm = document.getElementById('uploadForm');
if (uploadForm) {
    uploadForm.addEventListener('submit', function(e) {
        e.preventDefault();
        const name = document.getElementById('itemName').value;
        const price = document.getElementById('itemPrice').value;
        const details = document.getElementById('itemDetails').value;
        const imageFile = document.getElementById('itemImage').files[0];

        if (imageFile) {
            const reader = new FileReader();
            reader.onload = function() {
                const image = reader.result;
                const products = JSON.parse(localStorage.getItem('products')) || [];
                products.push({ name, price, details, image });
                localStorage.setItem('products', JSON.stringify(products));
                alert('Item uploaded successfully!');
                window.location.href = 'products.html';
            };
            reader.readAsDataURL(imageFile);
        }
    });
}

// Load products on page load
document.addEventListener('DOMContentLoaded', loadProducts);
```

### कैसे इस्तेमाल करें:
1. फाइलें बनाएं और `index.html` खोलें।
2. "Upload Your Item" पर क्लिक करें, डिटेल भरें, और अपलोड करें।
3. "Products" पेज पर जाएं – सभी अपलोड किए गए आइटम दिखेंगे।
4. किसी आइटम पर "Message Seller on WhatsApp" बटन पर क्लिक करें – WhatsApp खुल जाएगा और मैसेज जाएगा।
5. SEO के लिए, इसे ऑनलाइन होस्ट करें और Google में इंडेक्स करवाएं।

यदि आपको कोई बदलाव चाहिए (जैसे ज्यादा फीचर्स या डेटाबेस), तो बताएं! यह कोड पूरी तरह से फ्री है और आप इसे मॉडिफाई कर सकते हैं।
### फाइल स्ट्रक्चर:
1. `index.html` (होमपेज)
2. `upload.html` (अपलोड पेज)
3. `products.html` (प्रोडक्ट्स पेज)
4. `styles.css` (CSS फाइल)
5. `script.js` (JavaScript फाइल)

### कोड (कॉपी-पेस्ट करके फाइलें बनाएं):

#### 1. index.html
```html
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shekhar Zone - कुछ भी बेचो, ग्राहक सीधे WhatsApp पर!</title>
    <meta name="description" content="Shekhar Zone: Buy and sell anything like mobiles, clothes, shoes, electronics. Upload your items and connect via WhatsApp.">
    <meta name="keywords" content="Shekhar Zone, buy sell, mobiles, clothes, shoes, electronics, WhatsApp marketplace">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Shekhar Zone</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="products.html">Products</a>
            <a href="upload.html">Upload Item</a>
        </nav>
    </header>
    <main>
        <section class="hero">
            <h2>Shekhar Zone — कुछ भी बेचो, ग्राहक सीधे WhatsApp पर!</h2>
            <p>Upload your products and let customers message you directly on WhatsApp.</p>
            <a href="upload.html" class="btn upload-btn">Upload Your Item</a>
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Shekhar Zone. All rights reserved.</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
```

#### 2. upload.html
```html
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Upload Item - Shekhar Zone</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Shekhar Zone</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="products.html">Products</a>
            <a href="upload.html">Upload Item</a>
        </nav>
    </header>
    <main>
        <section class="upload-form">
            <h2>Upload Your Item</h2>
            <form id="uploadForm">
                <label for="itemName">Item Name (आइटम का नाम):</label>
                <input type="text" id="itemName" required>

                <label for="itemPrice">Price (कीमत):</label>
                <input type="number" id="itemPrice" required>

                <label for="itemDetails">Details (विवरण):</label>
                <textarea id="itemDetails" required></textarea>

                <label for="itemImage">Image (फोटो):</label>
                <input type="file" id="itemImage" accept="image/*" required>

                <button type="submit" class="btn">Upload</button>
            </form>
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Shekhar Zone. All rights reserved.</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
```

#### 3. products.html
```html
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Products - Shekhar Zone</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Shekhar Zone</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="products.html">Products</a>
            <a href="upload.html">Upload Item</a>
        </nav>
    </header>
    <main>
        <section class="products">
            <h2>Available Products</h2>
            <div id="productList"></div>
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Shekhar Zone. All rights reserved.</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
```

#### 4. styles.css
```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: lightblue;
    color: #333;
}

header {
    background-color: white;
    padding: 1rem;
    text-align: center;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

nav a {
    margin: 0 1rem;
    text-decoration: none;
    color: #007bff;
}

.hero {
    text-align: center;
    padding: 2rem;
    background-color: white;
    margin: 1rem;
    border-radius: 8px;
}

.btn {
    background-color: #25d366; /* WhatsApp green */
    color: white;
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    text-decoration: none;
    display: inline-block;
}

.upload-btn {
    margin-top: 1rem;
}

.upload-form {
    max-width: 600px;
    margin: 2rem auto;
    padding: 1rem;
    background-color: white;
    border-radius: 8px;
}

form label {
    display: block;
    margin-top: 1rem;
}

form input, form textarea {
    width: 100%;
    padding: 0.5rem;
    margin-top: 0.5rem;
}

.products {
    padding: 2rem;
}

.product-item {
    background-color: white;
    margin: 1rem 0;
    padding: 1rem;
    border-radius: 8px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.product-item img {
    max-width: 200px;
    height: auto;
}

footer {
    text-align: center;
    padding: 1rem;
    background-color: white;
}

/* Mobile responsive */
@media (max-width: 768px) {
    .hero h2 {
        font-size: 1.5rem;
    }
    .product-item {
        flex-direction: column;
    }
}
```

#### 5. script.js
```javascript
// Load products from localStorage
function loadProducts() {
    const products = JSON.parse(localStorage.getItem('products')) || [];
    const productList = document.getElementById('productList');
    if (productList) {
        productList.innerHTML = '';
        products.forEach(product => {
            const itemDiv = document.createElement('div');
            itemDiv.className = 'product-item';
            itemDiv.innerHTML = `
                <img src="${product.image}" alt="${product.name}">
                <h3>${product.name}</h3>
                <p>Price: ₹${product.price}</p>
                <p>${product.details}</p>
                <a href="https://wa.me/919236682603?text=${encodeURIComponent(`नमस्ते, मैंने आपका आइटम ${product.name} Shekhar Zone पर देखा है। क्या अभी उपलब्ध है?`)}" class="btn">Message Seller on WhatsApp</a>
            `;
            productList.appendChild(itemDiv);
        });
    }
}

// Handle upload form
const uploadForm = document.getElementById('uploadForm');
if (uploadForm) {
    uploadForm.addEventListener('submit', function(e) {
        e.preventDefault();
        const name = document.getElementById('itemName').value;
        const price = document.getElementById('itemPrice').value;
        const details = document.getElementById('itemDetails').value;
        const imageFile = document.getElementById('itemImage').files[0];

        if (imageFile) {
            const reader = new FileReader();
            reader.onload = function() {
                const image = reader.result;
                const products = JSON.parse(localStorage.getItem('products')) || [];
                products.push({ name, price, details, image });
                localStorage.setItem('products', JSON.stringify(products));
                alert('Item uploaded successfully!');
                window.location.href = 'products.html';
            };
            reader.readAsDataURL(imageFile);
        }
    });
}

// Load products on page load
document.addEventListener('DOMContentLoaded', loadProducts);
```

### कैसे इस्तेमाल करें:
1. फाइलें बनाएं और `index.html` खोलें।
2. "Upload Your Item" पर क्लिक करें, डिटेल भरें, और अपलोड करें।
3. "Products" पेज पर जाएं – सभी अपलोड किए गए आइटम दिखेंगे।
4. किसी आइटम पर "Message Seller on WhatsApp" बटन पर क्लिक करें – WhatsApp खुल जाएगा और मैसेज जाएगा।
5. SEO के लिए, इसे ऑनलाइन होस्ट करें और Google में इंडेक्स करवाएं।

यदि आपको कोई बदलाव चाहिए (जैसे ज्यादा फीचर्स या डेटाबेस), तो बताएं! यह कोड पूरी तरह से फ्री है और आप इसे मॉडिफाई कर सकते हैं।
