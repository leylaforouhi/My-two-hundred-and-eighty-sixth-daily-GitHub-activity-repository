def get_factors(numbe):
    if number <= 0:
        return []

    factors = []

    for divisor in range(1, int(number ** 0.5) + 1):
        if number % divisor == 0:
            factors.append(divisor)

            if divisor != number // divisor:
                factors.append(number // divisor)

    return sorted(factors)


if __name__ == "__main__":
    number = 36

    print("Number:", number)
    print("Factors:", get_factors(number))
