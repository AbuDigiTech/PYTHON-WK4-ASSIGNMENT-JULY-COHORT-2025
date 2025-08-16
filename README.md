def read_and_write_file(input_filename, output_filename):
    try:
        # Read the contents of the input file
        with open(input_filename, 'r') as input_file:
            content = input_file.read()

        # Modify the content (e.g., convert to uppercase)
        modified_content = content.upper()

        # Write the modified content to the output file
        with open(output_filename, 'w') as output_file:
            output_file.write(modified_content)

        print(f"File written successfully to {output_filename}")

    except FileNotFoundError:
        print(f"File {input_filename} not found.")
    except PermissionError:
        print(f"Permission denied to read or write file.")
    except Exception as e:
        print(f"An error occurred: {e}")

def main():
    input_filename = 'input.txt'
    output_filename = 'output.txt'
    read_and_write_file(input_filename, output_filename)

if __name__ == "__main__":
    main()

def read_file_with_error_handling():
    filename = input("Enter a filename: ")

    try:
        # Attempt to open and read the file
        with open(filename, 'r') as file:
            content = file.read()
            print(content)

    except FileNotFoundError:
        print(f"File {filename} not found.")
    except PermissionError:
        print(f"Permission denied to read file {filename}.")
    except Exception as e:
        print(f"An error occurred: {e}")

def main():
    read_file_with_error_handling()

if __name__ == "__main__":
    main()
