# cooking-lab-api

1. Clone the backend:
   ```sh
   git clone https://github.com/CookingLab/cooking-lab-api.git
   ```
2. Start the backend
   ```sh
    npm run dev
    ```

## API Endpoints

### Get Recipes

**Endpoint:** `/api/recipes`

**Method:** `GET`

**Description:** This endpoint retrieves recipes based on the specified parameters.

**Parameters:**

- `cuisineType` (required): The type of cuisine to filter recipes by.
- `mealType` (required): The type of meal to filter recipes by.
- `diet` (optional): An array of diet labels to filter recipes by. Multiple values can be provided.
- `health` (optional): An array of health labels to filter recipes by. Multiple values can be provided.
- `meat` (optional): A specific type of meat to filter recipes by.

**Example Request:**

```sh
GET /api/recipes?cuisineType=italian&mealType=dinner&diet=low-carb&health=gluten-free&meat=chicken
```

**Example Response:**

```json
{
  "label": "Chicken Parmesan",
  "image": "https://example.com/chicken-parmesan.jpg",
  "ingredients": ["chicken", "parmesan cheese", "tomato sauce"],
  "url": "https://example.com/chicken-parmesan-recipe"
}
```
