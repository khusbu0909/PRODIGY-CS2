from PIL import Image

def process_image(image_path, output_path, key):
    try:
        # Image ko open karein
        img = Image.open(image_path)
        pixels = img.load() # Pixels ka access lein
        
        width, height = img.size
        
        # Har ek pixel par loop chalayein
        for x in range(width):
            for y in range(height):
                # Pixel ke RGB values nikalein
                current_pixel = pixels[x, y]
                
                # Agar image RGB hai (3 channels)
                if len(current_pixel) == 3:
                    r, g, b = current_pixel
                    # Key ke sath XOR operation karein
                    pixels[x, y] = (r ^ key, g ^ key, b ^ key)
                # Agar image RGBA hai (4 channels - transparent background)
                elif len(current_pixel) == 4:
                    r, g, b, a = current_pixel
                    pixels[x, y] = (r ^ key, g ^ key, b ^ key, a)

        # Nayi image ko save karein
        img.save(output_path)
        print(f"Success! Image saved at: {output_path}")
        
    except Exception as e:
        print(f"Error: {e}")

# --- MAIN PROGRAM ---
if _name_ == "_main_":
    print("--- Pixel Manipulation Tool ---")
    choice = input("Enter 'E' for Encryption or 'D' for Decryption: ").upper()
    
    input_img = input("Enter input image path (e.g., photo.jpg): ")
    output_img = input("Enter output image name (e.g., encrypted.jpg): ")
    
    # Koyi bhi ek number chunein (0-255) jo aapki secret key hogi
    secret_key = int(input("Enter a secret key (Number between 1-255): "))
    
    if choice == 'E' or choice == 'D':
        process_image(input_img, output_img, secret_key)
    else:
        print("Invalid choice!")
