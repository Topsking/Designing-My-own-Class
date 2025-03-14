# Parent class
class Smartphone:
    def __init__(self, brand, model, price):
        self.brand = brand
        self.model = model
        self.price = price

    def make_call(self, number):
        print(f"Calling {number} from {self.model}...")

    def send_message(self, number, message):
        print(f"Sending message to {number}: {message}")

# Child class (Inheritance)
class GamingSmartphone(Smartphone):
    def __init__(self, brand, model, price, gpu):
        super().__init__(brand, model, price)
        self.gpu = gpu  # Additional attribute for gaming smartphones

    # Polymorphism: Overriding a method
    def make_call(self, number):
        print(f"Calling {number} in gaming mode on {self.model}!")

    # New method exclusive to GamingSmartphone
    def play_game(self, game_name):
        print(f"Playing {game_name} on {self.model} with {self.gpu} GPU.")

# Example usage
phone = Smartphone("Apple", "iPhone 14", 999)
gaming_phone = GamingSmartphone("Asus", "ROG Phone 6", 1299, "Adreno 730")

phone.make_call("123-456-7890")
gaming_phone.make_call("123-456-7890")
gaming_phone.play_game("PUBG")
ACTIVITY 2
# Base class
class Vehicle:
    def move(self):
        print("The vehicle is moving.")

# Car class (inherits from Vehicle)
class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

# Plane class (inherits from Vehicle)
class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

# Boat class (inherits from Vehicle)
class Boat(Vehicle):
    def move(self):
        print("Sailing 🚤")

# Example usage
vehicles = [Car(), Plane(), Boat()]

for vehicle in vehicles:
    vehicle.move()

