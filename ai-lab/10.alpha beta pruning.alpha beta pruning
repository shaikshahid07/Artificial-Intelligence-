
import math

# Define a simple game tree with alpha-beta pruning
def alpha_beta(node, depth, alpha, beta, is_maximizing):
    if not node['children']:
        return node['value']
    
    if is_maximizing:
        best_score = -math.inf
        for child in node['children']:
            score = alpha_beta(child, depth + 1, alpha, beta, False)
            best_score = max(score, best_score)
            alpha = max(alpha, best_score)
            if beta <= alpha:
                break  # Beta cutoff
        return best_score
    else:
        best_score = math.inf
        for child in node['children']:
            score = alpha_beta(child, depth + 1, alpha, beta, True)
            best_score = min(score, best_score)
            beta = min(beta, best_score)
            if beta <= alpha:
                break  # Alpha cutoff
        return best_score

# Example game tree
game_tree = {
    'is_maximizing': True,  # Maximizing player starts
    'value': None,  # Not used in non-leaf nodes
    'children': [
        {'is_maximizing': False, 'value': None, 'children': [
            {'is_maximizing': True, 'value': 1, 'children': []},
            {'is_maximizing': True, 'value': 2, 'children': []}
        ]},
        {'is_maximizing': False, 'value': None, 'children': [
            {'is_maximizing': True, 'value': 3, 'children': []},
            {'is_maximizing': True, 'value': 4, 'children': []}
        ]}
    ]
}

# Calculate the best score for the root node with alpha-beta pruning
best_score = alpha_beta(game_tree, 0, -math.inf, math.inf, True)
print("Best score for the maximizing player with Alpha-Beta Pruning:", best_score)
