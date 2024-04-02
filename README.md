try:
   
    with open("my_file.txt", "w") as f:
        f.write("Line 1:Hello!\n")
        f.write("Line 2: 1000001\n")
        f.write("Line 3: I love coding\n")

    print("Contents of my_file.txt:")
    with open("my_file.txt", "r") as f:
        contents = f.read()
        print(contents)

    with open("my_file.txt", "a") as f:
        f.write("Additional line1:Expore python \n")
        f.write("Additional line 2:Write code\n")
        f.write("Additional line 3:Enjoy!\n")

except FileNotFoundError:
    print("Error: The file does not exist.")

except PermissionError:
    print("Error: Permission denied to access the file.")

except Exception as e:
    print("An error occurred:", e)

finally:
    print("Execution succesfully completed.")
