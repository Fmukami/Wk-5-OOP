# Wk-5-OOP
Object oriented programming 

class Smartphone:
    def __init__(self, brand, model, storage, battery_life):
        # Constructor to initialize the object with unique values
        self.brand = brand
        self.model = model
        self.storage = storage
        self.battery_life = battery_life

    def display_info(self):
        # Method to display information about the smartphone
        print(f"Brand: {self.brand}")
        print(f"Model: {self.model}")
        print(f"Storage: {self.storage} GB")
        print(f"Battery Life: {self.battery_life} hours")

    def charge(self):
        # Simulating charging the phone
        print(f"{self.model} is charging...")

# Inheriting from Smartphone to create a specialized class
class GamingPhone(Smartphone):
    def __init__(self, brand, model, storage, battery_life, gpu, cooling_system):
        # Calling the parent constructor
        super().__init__(brand, model, storage, battery_life)
        # Additional attributes for gaming phone
        self.gpu = gpu
        self.cooling_system = cooling_system

    def display_info(self):
        # Overriding the display_info method to add gaming-specific details
        super().display_info()
        print(f"GPU: {self.gpu}")
        print(f"Cooling System: {self.cooling_system}")

    def run_game(self, game_name):
        # Unique method for GamingPhone
        print(f"Running {game_name} on {self.model} with high performance!")

# Creating instances of Smartphone and GamingPhone
phone1 = Smartphone("Apple", "iPhone 13", 128, 20)
gaming_phone = GamingPhone("Asus", "ROG Phone 5", 512, 16, "Adreno 660", "Active Cooling")

# Testing methods and attributes
phone1.display_info()
phone1.charge()

print("\n--- Gaming Phone Info ---")
gaming_phone.display_info()
gaming_phone.run_game("Call of Duty Mobile")
