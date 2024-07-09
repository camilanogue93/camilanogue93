from PIL import Image, ImageDraw, ImageFont

# Definindo as cores
turquoise = (64, 224, 208)
yellow = (255, 215, 0)
purple = (138, 43, 226)

# Criando uma nova imagem em branco
width, height = 1080, 1080
image = Image.new('RGB', (width, height), 'white')
draw = ImageDraw.Draw(image)

# Carregando a fonte
try:
    font_path = "/usr/share/fonts/truetype/dejavu/DejaVuSans-Bold.ttf"  # Caminho para a fonte (DejaVuSans)
    font = ImageFont.truetype(font_path, 60)
except IOError:
    font = ImageFont.load_default()

# Desenhando o gráfico da bio bem-feita
draw.rectangle([50, 50, width-50, height-50], outline=turquoise, width=10)
draw.text((150, 200), "Sua bio é o cartão de visitas do seu Instagram!", fill=purple, font=font)
draw.text((150, 300), "Seja claro e direto, destaque seu diferencial", fill=purple, font=font)
draw.text((150, 400), "e use emojis para chamar atenção.", fill=purple, font=font)
draw.text((150, 500), "Veja como uma bio bem-feita pode fazer a diferença!", fill=yellow, font=font)

# Salvando a imagem
image_path = "/mnt/data/post_exemplo_bio_instagram.png"
image.save(image_path)

image_path


