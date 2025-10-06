import itertools


distances = [
    [0, 10, 15, 20],  # distances from city 0 to other cities
    [10, 0, 35, 25],  # distances from city 1 to other cities
    [15, 35, 0, 30],  # distances from city 2 to other cities
    [20, 25, 30, 0]   # distances from city 3 to other cities
]

n = len(distances)

cities = range(n)
all_routes = itertools.permutations(cities)

min_route = None
min_cost = float('inf')

for route in all_routes:
    cost = 0
    for i in range(n - 1):
        cost += distances[route[i]][route[i + 1]]
    cost += distances[route[-1]][route[0]]  
    
    if cost < min_cost:
        min_cost = cost
        min_route = route

print("Best Route:", min_route)
print("Minimum Cost:", min_cost)
