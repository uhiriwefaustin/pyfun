#print("hello world")
#text=input("enter word:")
#print("it's chacters are"+len(text))
#print("enter five words")
#for a in range(5):
#    word=input("\n")
#for a in range(5): print(len(word))

def kajipo(text):
    # Define character mappings
    arr1 = "kajipotefu"
    arr2 = "akijopetuf"

    result = []
    for char in text:
        if char in arr1:
            index = arr1.index(char)
            result.append(arr2[index])
        elif char in arr2:
            index = arr2.index(char)
            result.append(arr1[index])
        else:
            result.append(char)  # Keep non-mapped characters unchanged

    return ''.join(result)

# Get user input
user_input = input("Enter text: ")

# Replace characters in the user input
result = kajipo(user_input)

print("Updated text:", result)

