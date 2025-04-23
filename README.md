import discord
from discord.ext import commands
import os


TOKEN = os.environ.get('YOU BOT TOKEN')

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix="!", intents=intents)

@bot.event
async def on_ready():
    print(f"bot is online as {bot.user}")
