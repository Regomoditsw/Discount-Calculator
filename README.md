# Discount-Calculator


def calculate_discount(price, discount_percent):
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        return price - discount_amount
    else:
        return price


try:
    price = float(input("Enter the original price: "))
    discount_percent = float(input("Enter the discount percentage: "))

    final_price = calculate_discount(price, discount_percent)

    if discount_percent >= 20:
        print(f"Discount applied. Final price: R{final_price:.2f}")
    else:
        print(f"No discount applied. Final price: R{final_price:.2f}")

except ValueError:
    print("Invalid input. Please enter numeric values.")
