Assignment 1
# Base class
class Smartphone:
    def __init__(self, brand, model, price):
        self.brand = brand
        self.model = model
        self.price = price

    def call(self, number):
        return f"Calling {number} from {self.model}."

    def send_message(self, number, message):
        return f"Sending '{message}' to {number} from {self.model}."

# Subclass demonstrating inheritance
class Smartwatch(Smartphone):
    def __init__(self, brand, model, price, strap_type):
        super().__init__(brand, model, price)
        self.strap_type = strap_type

    # Overriding a method to showcase polymorphism
    def call(self, number):
        return f"Initiating a call to {number} using the smartwatch {self.model}."

phone = Smartphone("TechBrand", "X200", 800)
print(phone.call("123-456-789"))

watch = Smartwatch("TechBrand", "W100", 300, "Leather")
print(watch.call("987-654-321"))

Assignment 2
# Base class
class Vehicle:
    def move(self):
        pass  # Placeholder for subclass behavior

# Subclass 1
class Car(Vehicle):
    def move(self):
        return "Driving 🚗"

# Subclass 2
class Plane(Vehicle):
    def move(self):
        return "Flying ✈️"

# Subclass 3
class Boat(Vehicle):
    def move(self):
        return "Sailing 🚤"

# Demonstrate polymorphism
vehicles = [Car(), Plane(), Boat()]
for vehicle in vehicles:
    print(vehicle.move())
