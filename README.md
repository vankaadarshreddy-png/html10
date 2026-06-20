# -------------------------------
# Dictionary Data Types Assignment
# -------------------------------

# Initialize empty dictionary for user profiles
user_profiles = {}

# Function to add a new user profile
def add_user(user_id, name):
    user_profiles[user_id] = name
    print(f"Added user: {user_id} -> {name}")
    print("Current profiles:", user_profiles)

# Function to retrieve a user's name by ID
def get_user(user_id):
    if user_id in user_profiles:
        print(f"User found: {user_id} -> {user_profiles[user_id]}")
    else:
        print(f"User ID {user_id} not found.")

# Function to update an existing user's name
def update_user(user_id, new_name):
    if user_id in user_profiles:
        user_profiles[user_id] = new_name
        print(f"Updated user {user_id} to new name: {new_name}")
    else:
        print(f"User ID {user_id} not found.")
    print("Current profiles:", user_profiles)

# Function to remove a user profile by ID
def remove_user(user_id):
    if user_id in user_profiles:
        removed_name = user_profiles.pop(user_id)
        print(f"Removed user: {user_id} -> {removed_name}")
    else:
        print(f"User ID {user_id} not found.")
    print("Current profiles:", user_profiles)


# -------------------------------
# Testing the functions
# -------------------------------
if __name__ == "__main__":
    # Add users
    add_user(101, "Alice")
    add_user(102, "Bob")
    add_user(103, "Charlie")

    # Retrieve users
    get_user(102)
    get_user(999)  # non-existent ID

    # Update user
    update_user(103, "Charlotte")
    update_user(200, "David")  # non-existent ID

    # Remove user
    remove_user(101)
    remove_user(500)  # non-existent ID
