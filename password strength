import re

def password_strength(password):
    """
    Assess the strength of a password based on length, uppercase and lowercase letters, numbers, and special characters.
    
    Args:
        password (str): The password to assess.
    
    Returns:
        str: The strength of the password (Weak, Medium, Strong).
    """
    length_criteria = len(password) >= 8
    uppercase_criteria = re.search(r'[A-Z]', password) is not None
    lowercase_criteria = re.search(r'[a-z]', password) is not None
    number_criteria = re.search(r'[0-9]', password) is not None
    special_character_criteria = re.search(r'[!@#$%^&*(),.?":{}|<>]', password) is not None

    # Calculate password strength
    strength_score = sum([length_criteria, uppercase_criteria, lowercase_criteria, number_criteria, special_character_criteria])

    if strength_score <= 2:
        return "Weak"
    elif strength_score == 3 or strength_score == 4:
        return "Medium"
    else:
        return "Strong"


if __name__ == "__main__":
    user_password = input("Enter your password: ")
    strength = password_strength(user_password)
    print(f"Your password strength is: {strength}")