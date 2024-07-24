# el-refaey-store
my website is to share the local products 
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>El Refaey Store</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>El Refaey Store</h1>
        <nav>
            <ul>
                <li><a href="#home">الرئيسية</a></li>
                <li><a href="#products">المنتجات</a></li>
                <li><a href="#contact">تواصل معنا</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="home">
            <h2>مرحبا بكم في El Refaey Store</h2>
            <p>استعرضوا منتجاتنا المميزة.</p>
        </section>
        <section id="products">
            <h2>المنتجات</h2>
            <div class="product-list">
                <!-- هنا يتم إضافة المنتجات -->
            </div>
        </section>
        <section id="contact">
            <h2>تواصل معنا</h2>
            <form>
                <label for="name">الاسم:</label>
                <input type="text" id="name" name="name" required>
                <label for="email">البريد الإلكتروني:</label>
                <input type="email" id="email" name="email" required>
                <label for="message">الرسالة:</label>
                <textarea id="message" name="message" required></textarea>
                <button type="submit">إرسال</button>
            </form>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 El Refaey Store. جميع الحقوق محفوظة.</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #f5f5f5;
    color: #333;
    margin: 0;
    padding: 0;
}

header {
    background-color: #4CAF50;
    color: white;
    padding: 1rem;
    text-align: center;
}

nav ul {
    list-style-type: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 10px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

main {
    padding: 2rem;
}

h2 {
    color: #4CAF50;
}

.product-list {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}

.product-item {
    background-color: white;
    border: 1px solid #ddd;
    padding: 1rem;
    width: calc(33.333% - 40px);
    box-sizing: border-box;
    text-align: center;
}

.product-item img {
    max-width: 100%;
    height: auto;
}

footer {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 1rem;
    position: fixed;
    width: 100%;
    bottom: 0;
}
document.addEventListener('DOMContentLoaded', () => {
    const products = [
        {
            name: 'منتج 1',
            image: 'product1.jpg',
            description: 'وصف المنتج 1',
            price: '100 جنيه'
        },
        {
            name: 'منتج 2',
            image: 'product2.jpg',
            description: 'وصف المنتج 2',
            price: '200 جنيه'
        },
        {
            name: 'منتج 3',
            image: 'product3.jpg',
            description: 'وصف المنتج 3',
            price: '300 جنيه'
        }
    ];

    const productList = document.querySelector('.product-list');

    products.forEach(product => {
        const productItem = document.createElement('div');
        productItem.classList.add('product-item');
        
        productItem.innerHTML = `
            <img src="${product.image}" alt="${product.name}">
            <h3>${product.name}</h3>
            <p>${product.description}</p>
            <p>السعر: ${product.price}</p>
        `;
        
        productList.appendChild(productItem);
    });
});
