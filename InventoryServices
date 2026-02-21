namespace InventoryApp.Services
{
    public class InventoryService
    {
        private string[,] products;
        private int[] initialStock;

        public InventoryService()
        {
            products = new string[2, 3];

            // Product Names
            products[0, 0] = "";
            products[0, 1] = "Milk";
            products[0, 2] = "Bread";

            // Stock Quantities
            products[1, 0] = "10";
            products[1, 1] = "5";
            products[1, 2] = "20";

            // Store original stock for reset
            initialStock = new int[3];
            for (int i = 0; i < 3; i++)
            {
                initialStock[i] = int.Parse(products[1, i]);
            }
        }

        public string[,] GetInventory()
        {
            return products;
        }

        public void UpdateStock(int index, int newStock)
        {
            if (index >= 0 && index < 3)
            {
                products[1, index] = newStock.ToString();
            }
        }

        public void ResetInventory()
        {
            for (int i = 0; i < 3; i++)
            {
                products[1, i] = initialStock[i].ToString();
            }
        }
    }
}
