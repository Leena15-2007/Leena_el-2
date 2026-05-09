<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>API Documentation</title>
<link rel="stylesheet" href="style.css">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  *{  margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}
html{
    scroll-behavior:smooth;
}
body{
    background:#0f172a;
    color:#e2e8f0;
    display:flex;
}
.sidebar{
    width:280px;
    height:100vh;
    position:fixed;
    top:0;
    left:0;
    overflow-y:auto;
    background:linear-gradient(180deg,#1e1b4b,#312e81,#0f172a);
    padding:25px;
    border-right:1px solid rgba(255,255,255,0.1);
}
.logo{
    font-size:28px;
    font-weight:700;
    color:#ffffff;
    margin-bottom:30px;
}
.logo span{
    color:#60a5fa;
}
.sidebar h3{
    margin-bottom:15px;
    color:#93c5fd;
    font-size:18px;
}
.sidebar ul{
    list-style:none;
}
.sidebar ul li{
    margin:12px 0;
}
.sidebar ul li a{
    text-decoration:none;
color:#cbd5e1;
    font-size:15px;
    padding:10px 14px;
    display:block;
    border-radius:10px;
    transition:0.3s;
}
.sidebar ul li a:hover{
    background:#2563eb;
    color:#fff;
    transform:translateX(5px);
}
.main-content{
    margin-left:280px;
    width:calc(100% - 280px);
    padding:40px;
}
.hero{
    background:linear-gradient(135deg,#2563eb,#7c3aed);
    padding:40px;
    border-radius:20px;
    margin-bottom:40px;
    box-shadow:0 10px 30px rgba(0,0,0,0.3);
}
.hero h1{
    font-size:45px;
    margin-bottom:15px;
}
.hero p{
    font-size:17px;
    line-height:1.7;
    color:#e0e7ff;
}
.section{
    margin-bottom:60px;
}
.section-title{
    font-size:32px;
    margin-bottom:20px;
    color:#93c5fd;
    position:relative;
}
.section-title::after{
    content:"";
    width:80px;
    height:4px;
    background:#3b82f6;
    position:absolute;
    left:0;
    bottom:-8px;
    border-radius:10px;
}.section p{
    margin-top:20px;
    line-height:1.8;
    color:#cbd5e1;
}
.card{
    background:#1e293b;
    padding:25px;
    border-radius:18px;
    margin-top:25px;
    border:1px solid rgba(255,255,255,0.08);
    transition:0.4s;
}
.card:hover{
    transform:translateY(-5px);
    box-shadow:0 10px 20px rgba(0,0,0,0.3);
}
.code-box{
    background:#020617;
    border-radius:15px;
    padding:20px;
    margin-top:20px;
    overflow-x:auto;
    position:relative;
}
.copy-btn{
    position:absolute;
    top:15px;
    right:15px;
    background:#2563eb;
    border:none;
    color:white;
    padding:8px 15px;
    border-radius:8px;
    cursor:pointer;
    transition:0.3s;
}
.copy-btn:hover{
    background:#1d4ed8;
}
pre{white-space:pre-wrap;
    color:#93c5fd;
    font-size:14px;
    line-height:1.7;
}
.table-container{
    overflow-x:auto;
    margin-top:20px;
}
table{
    width:100%;
    border-collapse:collapse;
    min-width:700px;
    background:#0f172a;
    border-radius:12px;
    overflow:hidden;

}
table th{
    background:#2563eb;
    color:white;
    padding:16px;
    text-align:left;
}
table td{
  padding:16px;
    border-bottom:1px solid rgba(255,255,255,0.08);
    color:#cbd5e1;
}

table tr:hover{
    background:#1e293b;
}
.btn{
    display:inline-block;
    margin-top:20px;
    padding:12px 22px;
    background:linear-gradient(135deg,#3b82f6,#7c3aed);
    color:white;
    text-decoration:none;
    border-radius:12px;
    transition:0.3s;
}
.btn:hover{
    transform:scale(1.05);
}
.alert{
    margin-top:20px;
    background:#172554;
    border-left:5px solid #3b82f6;
    padding:20px;
    border-radius:10px;
    color:#dbeafe;
}
.footer{
    margin-top:80px;
    text-align:center;
    padding:30px;
    color:#94a3b8;
    border-top:1px solid rgba(255,255,255,0.1);
}
.search-box{
    margin-bottom:30px;
}
.search-box input{
    width:100%;
    padding:15px;
    border:none;
    border-radius:12px;
    background:#1e293b;
    color:white;
    font-size:15px;
  








  outline:none;
}
.search-box input::placeholder{

    color:#94a3b8;
}
@media(max-width:900px){
    .sidebar{
        width:100%;
        height:auto;
        position:relative;
    }
    .main-content{
        margin-left:0;
        width:100%;
  padding:20px;
    }
    body{
        flex-direction:column;
    }
    .hero h1{
        font-size:32px;
    }}
</head>

<body>
<div class="sidebar">
    <div class="logo">
     API <span>Docs</span>
    </div>
    <h3>Documentation</h3>
    <ul>
        <li><a href="#intro">Introduction</a></li>
        <li><a href="#auth">Authentication</a></li>
        <li><a href="#users">Users API</a></li>
        <li><a href="#products">Products API</a></li>
        <li><a href="#orders">Orders API</a></li>
        <li><a href="#errors">Error Codes</a></li>
        <li><a href="#faq">FAQ</a></li>
    </ul>
  </div>
  <div class="main-content">
  <div class="search-box">
  <input type="text" id="searchInput" placeholder="Search documentation...">
  </div>

  <div class="hero">
  <h1>Developer API Documentation</h1>
  <p>
            Build powerful applications using our REST API.
            This documentation provides all endpoints, request methods,
            authentication details, parameters, and response examples
            needed to integrate successfully.
    </p>
    <a href="#intro" class="btn">Get Started</a>
    </div>
    <section class="section" id="intro">
        <h2 class="section-title">Introduction</h2>
        <p>
Welcome to the API documentation portal. This API helps developers manage users,    products, authentication, and orders securely.
        </p>
        <div class="card">
            <h3>Base URL</h3>
            <div class="code-box">
<button class="copy-btn">Copy</button>
<pre><code>https://api.example.com/v1</code></pre>
            </div>
        </div>
 <div class="alert">
 Make sure all requests include the correct authentication token.
    </div>
    </section>
    <section class="section" id="auth">
        <h2 class="section-title">Authentication</h2>
        <p>
            Authentication is performed using API keys.
            Include your API key inside the Authorization header.
        </p>
        <div class="card">
            <h3>Example Request</h3>
            <div class="code-box">
                <button class="copy-btn">Copy</button>
    <pre><code>GET /api/users

    Authorization: Bearer abc123xyz

    Content-Type: application/json</code></pre>
            </div>
        </div>
     </section>
     <section class="section" id="users">
        <h2 class="section-title">Users API</h2>
        <div class="card">
            <h3>Create User</h3>
            <div class="code-box">
                <button class="copy-btn">Copy</button>
   <pre><code>POST /users
   </code></pre>
   </div>
        </div>
    </section>
    <section class="section" id="products">
        <h2 class="section-title">Products API</h2>
        <div class="card">
            <h3>Add Product</h3>
            <div class="code-box">
                <button class="copy-btn">Copy</button>
   <pre><code>POST /products
   </code></pre>
            </div>
        </div>
   <div class="table-container">
           <table border="1" cellspacing="0"
             cellpadding="15" width="50%">
                <tr>
                    <th>Field</th>
                    <th>Type</th>
                    <th>Required</th>
                </tr>
                <tr>
                    <td>title</td>
                    <td>string</td>
                    <td>Yes</td>
                </tr>
                <tr>
                    <td>price</td>
                    <td>number</td>
                    <td>Yes</td>
                </tr>
                <tr>
                    <td>stock</td>
                    <td>number</td>
                    <td>No</td>
                </tr></table>
        </div>
     </section>
     <section class="section" id="orders">
        <h2 class="section-title">Orders API
     </h2>
        <p>
            Order endpoints are used to create,
            track, and manage customer orders.
        </p>
        <div class="card">
            <h3>Create Order</h3>
            <div class="code-box">
                <button class="copy-btn">Copy</button>
     <pre><code>POST /orders
     </code></pre>
            </div></div>
        <div class="card">
            <h3>Track Order</h3>
            <div class="code-box">
                <button class="copy-btn">Copy</button>
     <pre><code>GET /orders/track/1001</code></pre>
            </div>
     </div>
    </section>
    <section class="section" id="errors">
        <h2 class="section-title">Error Codes</h2>
        <p>API errors return standard HTTP status codes.</p>
        <div class="table-container">
<table border="1" cellspacing="0"
                cellpadding="15" width="70%">
                <tr><th>Status Code</th>
                    <th>Meaning</th>
                    <th>Description</th></tr>
                <tr>
     <td>200</td>
                    <td>Success</td>
                    <td>Request completed successfully</td>
                </tr>
                <tr>
     <td>400</td>
                    <td>Bad Request</td>
                    <td>Invalid parameters</td>
                </tr>
                <tr>
     <td>401</td>
                    <td>Unauthorized</td>
      <td>Invalid API key</td></tr>
                <tr><td>404</td>
                    <td>Not Found</td>
                    <td>Requested resource not found</td>
                </tr>
                <tr>
                    <td>500</td>
                    <td>Server Error</td>
                    <td>Internal server issue</td>
                </tr></table>
        </div>
        </section>
 <section class="section" id="faq">
        <h2 class="section-title">Frequently Asked Questions</h2>
        <div class="card">
            <h3>How do I get an API key?</h3>

 <p>
Register on the developer portal and create an application
                to receive your API key.</p>
        </div>
        <div class="card">
            <h3>What format does the API return?</h3>
            <p>All responses are returned in JSON format.</p>
        </div>
        <div class="card">
            <h3>Is HTTPS required?</h3>
            <p>Yes, HTTPS is mandatory for all API requests.</p>
        </div>
    </section>
    <div class="footer">
        <p>© 2026 API Documentation. All Rights Reserved.</p>
    </div>
</div>
</body>
</html>
