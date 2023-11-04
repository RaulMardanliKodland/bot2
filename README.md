import discord
from discord.ext import commands
import os
import random

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='$', intents=intents)

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def throwplastic(ctx):
    await ctx.send(f'Throw it to the recycle bin')

@bot.command()
async def throwbattery(ctx):
    await ctx.send(f'Throw it to the recycle bin')

@bot.command()
async def throwmetal(ctx):
    await ctx.send(f'Throw it to the recycle bin')

@bot.command()
async def throwpaper(ctx):
    await ctx.send(f'Throw it to any an ordinary bin')

@bot.command()
async def throwglass(ctx):
    await ctx.send(f'Throw it to the recycle bin')

@bot.command()
async def info(ctx):
    await ctx.send(f'I am a bot which will help you with recycling stuff!')

bot.run("")
