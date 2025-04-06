# week-3-assignment
assignment
def calculate_discount(price, discount_percent):
    """
    Returns the price after applying discount_percent if it is 20% or higher;
    otherwise returns the original price.
    """
    if discount_percent >= 20:
        # apply discount: final = price – (price × discount_percent/100)
        return price * (1 - discount_percent / 100)  # :contentReference[oaicite:0]{index=0}
    else:
        return price

def main():
    try:
        price = float(input("Enter original price: "))
        discount_percent = float(input("Enter discount percentage: "))
    except ValueError:
        print("Invalid input. Please enter numeric values.")
        return

    final_price = calculate_discount(price, discount_percent)

    if discount_percent >= 20:
        print(f"Final price after {discount_percent:.0f}% discount: {final_price:.2f}")
    else:
        print(f"No discount applied. Original price: {price:.2f}")

if __name__ == "__main__":
    main()

