## RSA Encryption and Decryption for Images

### Overview
This Python code demonstrates RSA encryption and decryption techniques applied to images. RSA (Rivest-Shamir-Adleman) is a public-key cryptosystem widely used for secure data transmission. In this example, we encrypt individual RGB values of each pixel in the image to change its color and then decrypt it to retrieve the original color.

### Steps

1. **Generate Prime Numbers (p, q):** Two large prime numbers (p, q) are generated randomly.
2. **Calculate N and Euler's Totient:** N is calculated as the product of p and q, and Euler's Totient function is calculated as (p-1)*(q-1).
3. **Find E:** E is generated such that it is coprime with Euler's Totient.
4. **Find D:** D is calculated using the Extended Euclidean Algorithm, satisfying the condition (D*E) mod (Euler's Totient) = 1.
5. **Encryption:** Each pixel's RGB values are encrypted using the formula C = P^E mod (N), where P is the original pixel value.
6. **Decryption:** Encrypted RGB values are decrypted using the formula P = C^D mod (N) to retrieve the original pixel values.
7. **Output:** Encrypted and decrypted images are saved as `encrypted_image.jpg` and `decrypted_image.jpg`, respectively.

### Efficiency
This encryption process is efficient for smaller images compared to larger images due to the computational complexity involved in RSA encryption and decryption operations. RSA is not efficient when working with images that have a high pixel density.

### Files
- **RSA_rgb.ipynb:** Contains the source code for encryption and decryption.

### Dependencies
- OpenCV (`cv2`)
- NumPy (`numpy`)
- Matplotlib (`matplotlib`)
- SymPy (`sympy`)

### Usage
1. Ensure you have all the dependencies installed.
2. Run the `RSA_rgb.ipynb` notebook to perform encryption and decryption on your images.

### Note
- Ensure the image file (`aadhar.jpg` in this case) exists in the same directory as the notebook or provide the correct path to the image file.
- Adjust the value of `length` for the desired bit length of prime numbers generated.
