# BestBuy API Documentation

## Overview
This API provides access to BestBuy product data, including search functionality, product details, reviews, pricing, and recommendations. The API is available through RapidAPI platform.

## Getting Started

### Prerequisites
1. Create a RapidAPI account at https://rapidapi.com
2. Subscribe to the [BestBuy API](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/bestbuy-usa)
3. Obtain your API key from RapidAPI dashboard

### Authentication
Include your RapidAPI key in the request headers:
```
X-RapidAPI-Key: YOUR_API_KEY
```

## API Endpoints

### Product Search
**GET** `/search`
Search for products in BestBuy's catalog.

Parameters:
- `query` (required): Search term
- `page` (optional): Page number (default: 1)

### Product Reviews
**GET** `/product/review`
Get product reviews.

Parameters:
- `sku` (required): Product SKU
- `page` (optional): Page number (default: 1)
- `perPage` (optional): Results per page (default: 20)

### Product Review Summary
**GET** `/product/review/summary`
Get summarized review statistics for a product.

Parameters:
- `skuId` (required): Product SKU

### Live Events
**GET** `/live-events`
Retrieve current live events or deals.

No parameters required.

### Product Pricing
**GET** `/product/price`
Get current product pricing.

Parameters:
- `sku` (required): Product SKU

### Product Pricing v2
**GET** `/product/price/v2`
Get enhanced product pricing information.

Parameters:
- `sku` (required): Product SKU

### Similar Products
**GET** `/product/similar`
Get recommended similar products.

Parameters:
- `sku` (required): Product SKU
- `limit` (optional): Number of recommendations (default: 20)

### Popular Terms
**GET** `/product/popularterms`
Get trending search terms.

No parameters required.

### Search Suggestions
**GET** `/search/suggestions`
Get search suggestions based on input.

Parameters:
- `query` (required): Search term
- `limit` (optional): Number of suggestions (default: 20)

### Short Product Description
**GET** `/product/description/short`
Get brief product descriptions.

Parameters:
- `skuIds` (required): Product SKU(s)

### Full Product Description
**GET** `/product/description`
Get detailed product description.

Parameters:
- `productUrl` (required): Product URL

### Gift With Purchase
**GET** `/product/gifts`
Get available gifts with purchase.

Parameters:
- `skuId` (required): Product SKU

### Product Description with Variations
**GET** `/product/description/short/v2`
Get product description including variations.

Parameters:
- `skuId` (required): Product SKU

### Trending Categories
**GET** `/categories/trending`
Get currently trending product categories.

No parameters required.

## Example Usage

```javascript
const axios = require('axios');

const options = {
  method: 'GET',
  url: 'https://bestbuy-usa.p.rapidapi.com/product/price',
  params: {
    sku: '6535453'
  },
  headers: {
    'X-RapidAPI-Key': 'YOUR_API_KEY',
    'X-RapidAPI-Host': 'https://bestbuy-usa.p.rapidapi.com'
  }
};

try {
  const response = await axios.request(options);
  console.log(response.data);
} catch (error) {
  console.error(error);
}
```

## Error Handling
The API returns standard HTTP status codes:
- 400: Bad Request - Missing required parameters
- 401: Unauthorized - Invalid API key
- 404: Not Found - Resource not found
- 500: Internal Server Error

Error responses follow this format:
```json
{
  "error": {
    "message": "Error message description",
    "code": "400"
  }
}
```

## Support
Need assistance or a custom plan? Reach out to us at pintoflowpt@gmail.com or send us a private message directly on RapidAPI. We're here to help!


---


### BestBuy: Your One-Stop Shop for Electronics and More

BestBuy is a leading retailer specializing in electronics, home appliances, entertainment, and a wide range of cutting-edge technology products. Founded in 1966, the company has become a trusted name in providing innovative solutions for customers looking to enhance their lives with modern technology. With a strong presence in both physical stores and online platforms, BestBuy continues to serve millions of customers with high-quality products and exceptional service.

---

#### **What BestBuy Offers**

**1. Electronics:**  
BestBuy boasts an extensive selection of electronics, ranging from the latest smartphones, laptops, and tablets to state-of-the-art TVs, gaming consoles, and audio equipment. Whether you're looking for a powerful gaming PC or the newest wearable technology, BestBuy ensures you have access to top brands and the latest innovations.

**2. Home Appliances:**  
From refrigerators and washing machines to air purifiers and smart thermostats, BestBuy's inventory caters to every home improvement need. Their range of energy-efficient appliances makes it easy for customers to find products that are both high-performing and environmentally conscious.

**3. Entertainment:**  
BestBuy provides a wide array of entertainment options, including DVDs, Blu-rays, video games, and streaming devices. Movie buffs, gamers, and music enthusiasts alike can find what they need to create the ultimate entertainment experience.

**4. Smart Home Solutions:**  
The rise of smart home technology has made life more convenient than ever, and BestBuy is at the forefront of this trend. They offer products such as smart lights, security cameras, voice assistants, and smart locks, making it easy to automate and secure your home.

**5. Health & Fitness:**  
For those committed to staying active, BestBuy offers fitness trackers, smartwatches, and personal care devices. With brands like Fitbit, Garmin, and Apple, you can track your fitness goals and maintain a healthy lifestyle.

**6. Customer Support Services:**  
BestBuy is known for its exceptional customer support. Services like Geek Squad provide expert installation, repair, and troubleshooting for your devices, ensuring they work seamlessly for years to come.

---

#### **Why Shop at BestBuy?**

**1. Competitive Prices:**  
BestBuy frequently offers discounts and deals, ensuring you get the best value for your money. With price-matching guarantees, you can shop with confidence knowing you're getting a great deal.

**2. Easy Online Shopping Experience:**  
Their user-friendly website allows customers to browse products, compare specifications, read reviews, and make purchases with ease. BestBuy also provides flexible delivery options, including same-day delivery and in-store pickup.

**3. Reward Programs:**  
BestBuy’s My Best Buy program offers exclusive perks, such as points for every dollar spent, early access to sales, and free shipping on qualifying orders.

**4. Sustainable Practices:**  
BestBuy is committed to sustainability. They have implemented initiatives to reduce carbon emissions, recycle electronics, and promote energy-efficient products.

**5. Accessibility:**  
With hundreds of physical locations and a robust online presence, BestBuy ensures that customers can easily access their products and services no matter where they are.

---

#### **FAQs About BestBuy**

**1. What are BestBuy’s store hours?**  
Store hours vary by location. It's best to check the specific hours of your local BestBuy store on their website or by contacting them directly.

**2. Does BestBuy offer financing options?**  
Yes, BestBuy provides financing through the My Best Buy Credit Card and other options. These programs allow customers to make purchases and pay over time, often with promotional interest-free periods.

**3. Can I return a product purchased from BestBuy?**  
BestBuy has a flexible return policy, typically allowing returns within 15 days of purchase for most items. My Best Buy Elite and Elite Plus members enjoy extended return periods. Certain conditions apply, so it's recommended to review their return policy on the website.

**4. Does BestBuy price match?**  
Yes, BestBuy offers a price match guarantee. If you find a lower price from a local competitor or major online retailer, BestBuy will match the price, subject to specific terms and conditions.

**5. What services does Geek Squad provide?**  
Geek Squad provides various services, including setup and installation, device repairs, data recovery, and software troubleshooting. Their experts are trained to handle issues across multiple devices and brands.

**6. Can I order online and pick up in-store?**  
Absolutely! BestBuy offers an in-store pickup option for online orders. Simply select this option during checkout, and you'll be notified when your order is ready for pickup.

**7. Does BestBuy ship internationally?**  
Currently, BestBuy primarily ships within the United States, though they may offer international shipping for select products. Customers outside the U.S. should check the BestBuy website for specific availability.

**8. What is the My Best Buy program?**  
The My Best Buy program is a free membership that rewards customers with points for every purchase. Members also gain access to exclusive offers, early sales, and free shipping on qualifying orders.

**9. Does BestBuy offer extended warranties?**  
Yes, BestBuy provides extended warranties and protection plans through their Geek Squad Protection service. These plans cover a wide range of issues, including accidental damage and product defects.

**10. How can I contact BestBuy customer service?**  
You can contact BestBuy’s customer service via phone, live chat on their website, or by visiting a local store. Their support team is available to assist with inquiries about products, orders, and services.

---


