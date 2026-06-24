user_profiles = {}
def add_user(user_id, user_name):
    user_profiles[user_id] = user_name
    print(f"User added: {user_id} -> {user_name}")
    print("Current Profiles:", user_profiles)
def get_user(user_id):
    if user_id in user_profiles:
        print(f"User found: {user_id} -> {user_profiles[user_id]}")
    else:
        print(f"Error: User ID {user_id} not found.")
def update_user(user_id, new_name):
    if user_id in user_profiles:
        user_profiles[user_id] = new_name
        print(f"User updated: {user_id} -> {new_name}")
    else:
        print(f"Error: Cannot update. User ID {user_id} not found.")
    print("Current Profiles:", user_profiles)
def remove_user(user_id):
    if user_id in user_profiles:
        removed_name = user_profiles.pop(user_id)
        print(f"User removed: {user_id} -> {removed_name}")
    else:
        print(f"Error: Cannot remove. User ID {user_id} not found.")
    print("Current Profiles:", user_profiles)
add_user(101, "Alice")
add_user(102, "Bob")
get_user(101)
get_user(999)  
update_user(102, "Robert")
update_user(999, "Charlie")  

# Remove user
remove_user(101)
remove_user(999)  
