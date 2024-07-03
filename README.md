import matplotlib.pyplot as plt
from PIL import Image, ImageDraw, ImageFont

# Create a blank image with white background
width, height = 1280, 640
image = Image.new('RGB', (width, height), 'white')
draw = ImageDraw.Draw(image)

# Load a font
font_path = "/usr/share/fonts/truetype/dejavu/DejaVuSans-Bold.ttf"  # Adjust path as necessary
font = ImageFont.truetype(font_path, 50)
font_small = ImageFont.truetype(font_path, 30)

# Add text
draw.text((50, 50), "Emir Bráz", fill="black", font=font)
draw.text((50, 150), "Federal University of Santa Catarina", fill="black", font=font_small)
draw.text((50, 200), "Computer Engineering", fill="black", font=font_small)
draw.text((50, 300), "Interests:", fill="black", font=font_small)
draw.text((50, 350), "- Hardware", fill="black", font=font_small)
draw.text((50, 400), "- Semiconductor", fill="black", font=font_small)
draw.text((50, 450), "- Silicon", fill="black", font=font_small)
draw.text((50, 500), "- Game Developing", fill="black", font=font_small)
draw.text((50, 550), "- Backend Developing", fill="black", font=font_small)

# Save the image
image_path = "/mnt/data/github_cover.png"
image.save(image_path)
image.show()
