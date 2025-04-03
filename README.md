# Faltu-pila
This is a paid bot using for file rename
TOKEN = '5789405678:AAE0_itrWHvnOos86GxPXXNh6QJd6oI9Yeo'
bot = Bot(token=TOKEN)

# Function to send a file with a custom thumbnail
def send_file_with_thumbnail(chat_id, file_path, thumbnail_path):
try:
# Open the file you want to send
file = InputFile(file_path)

# Open the thumbnail you want to send along with the file
thumbnail = InputFile(thumbnail_path)

# Send the file with the thumbnail as a photo
bot.send_document(
chat_id=chat_id, # ID of the chat you want to send the file to
document=file,
thumb=thumbnail # Custom thumbnail
)

print("File with thumbnail sent successfully!")

except TelegramError as e:
print(f"Error: {e}")

# Example usage
chat_id = 'YOUR_CHAT_ID' # You can get the chat ID of your channel/group
file_path = 'path_to_your_file.pdf' # Replace with the path to your file
thumbnail_path = 'path_to_your_thumbnail_image.jpg' # Replace with the path to your thumbnail image

send_file_with_thumbnail(chat_id, file_path, thumbnail_path)
