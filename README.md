# Product Display Project

This project displays products in a grid layout with search functionality and image modal viewing.

## Project Structure

- All images are stored in the `images` folder
- Each product has its own folder named by product ID (e.g., P001, P002, etc.)
- Each product folder contains all images for that product
- CSS styles are in the `css` folder
- JavaScript files are in the `js` folder:
  - `products.js`: Contains all product data
  - `script.js`: Handles UI logic and interactions

## Image Naming Convention

- Thumbnail (displayed in product list): `image1.jpg`
- Additional images (displayed in modal): `image2.jpg`, `image3.jpg`, etc.

## How to Add New Product Images

1. Create a new folder in the `images` directory with the product ID as the name
2. Place product images in that folder
3. Add product information in `js/products.js` using the following format:

```javascript
{
    id: "ProductID",
    name: "Product Name",
    images: [
        "images/ProductID/image1.jpg",
        "images/ProductID/image2.jpg",
        // More images...
    ],
    thumbnail: "images/ProductID/image1.jpg",
    prices: {
        kigali: "Price",
        muhanga: "Price"
    }
}
```

## Product Configuration

All product information is stored in the `js/products.js` file. Each product object has the following structure:

```javascript
{
    id: "Unique product identifier",
    name: "Product display name",
    images: [
        "Array of image paths for the product modal",
    ],
    thumbnail: "Path to the thumbnail image for product card",
    prices: {
        kigali: "Price in Kigali location",
        muhanga: "Price in Muhanga location"
    }
}
```

### Example Product Configuration

```javascript
{
    id: "P001",
    name: "Sony WH-1000XM4 Wireless Headphones",
    images: [
        "images/P001/image1.jpg",
        "images/P001/image2.jpg",
        "images/P001/image3.jpg"
    ],
    thumbnail: "images/P001/image1.jpg",
    prices: {
        kigali: "183,600 RF",
        muhanga: "204,000 RF"
    }
}
```

## Important Notes

- Ensure images are in JPG format
- Recommended thumbnail size: 300x200 pixels
- Recommended modal image size: 600x400 pixels
- Image filenames must match the paths referenced in the code