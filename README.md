# ass--4

task 1.py
filename = "sample.txt"

try:
    with open(filename, 'r') as file:
        print("Reading file content:")
        line_num = 1
        for line in file:
            print(f"Line {line_num}: {line.strip()}")
            line_num += 1
except FileNotFoundError:
    print(f"Error: The file '{filename}' was not found.")

    task 2.py
    filename = "output.txt"

# Step 1: Write user input to the file
text_to_write = input("Enter text to write to the file: ")
with open(filename, 'w') as file:
    file.write(text_to_write + '\n')
print("Data successfully written to output.txt.")

# Step 2: Append additional user input
text_to_append = input("Enter additional text to append: ")
with open(filename, 'a') as file:
    file.write(text_to_append + '\n')
print("Data successfully appended.")

# Step 3: Read and display the final content
print("\nFinal content of output.txt:")
with open(filename, 'r') as file:
    print(file.read())
