# Prime-Numbers-in-Python-Project
During this Prime Numbers in Python project, you’ll devise a program for identifying such numbers.
#%%
def is_prime(n):
    # Handle edge cases
    if n <= 1:
        return False
    if n == 2:
        return True
    if n % 2 == 0:
        return False

    # Check odd divisors up to sqrt(n)
    for i in range(3, int(n**0.5) + 1, 2):
        if n % i == 0:
            return False

    return True
#%%
print(is_prime(7))   # True
print(is_prime(10))  # False
#%%
def is_prime(n):
    if n <= 1:
        return False
    if n == 2:
        return True
    if n % 2 == 0:
        return False
    for i in range(3, int(n**0.5) + 1, 2):
        if n % i == 0:
            return False
    return True

count = sum(1 for i in range(100, 152) if is_prime(i))
print(count)  # Output: 11
#%%

