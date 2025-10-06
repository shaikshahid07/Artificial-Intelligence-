from itertools import permutations

# Function to check if a given assignment is valid for SEND + MORE = MONEY
def is_valid(s, e, n, d, m, o, r, y):
    send = s * 1000 + e * 100 + n * 10 + d
    more = m * 1000 + o * 100 + r * 10 + e
    money = m * 10000 + o * 1000 + n * 100 + e * 10 + y
    return send + more == money

# Function to solve the cryptarithmetic problem
def solve_cryptarithmetic():
    letters = 'sendmory'
    for perm in permutations(range(10), 8):  # Generate permutations of 8 digits
        s, e, n, d, m, o, r, y = perm
        if s != 0 and m != 0:  # Leading digits can't be zero
            if is_valid(s, e, n, d, m, o, r, y):
                print(f"SEND = {s}{e}{n}{d}")
                print(f"MORE = {m}{o}{r}{e}")
                print(f"MONEY = {m}{o}{n}{e}{y}")
                return

# Call the solver
solve_cryptarithmetic()
