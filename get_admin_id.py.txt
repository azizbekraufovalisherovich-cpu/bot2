from aiogram import Bot, Dispatcher, types
from aiogram.utils import executor

BOT_TOKEN = 8043701343:AAG2MVo_dQbiSsSE-_-AMVSHVxEI7rMo2i0  # Bu yerga BotFather'dan olgan tokeningizni yozing
bot = Bot(token=BOT_TOKEN)
dp = Dispatcher(bot)

@dp.message_handler(commands=["start"])
async def start(message: types.Message):
    await message.answer(f"Sizning Telegram ID: {message.from_user.id}")

if __name__ == "__main__":
    executor.start_polling(dp, skip_updates=True)
