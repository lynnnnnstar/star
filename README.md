import TelegramBot from 'node-telegram-bot-api';
const token = '506437544:AAGZ8s201ahOwTnjlUZKTWe2pO2v8NpB2v4';
const bot = new TelegramBot(token, { polling: true });
bot.onText(/\/start/, message => {
  console.log(message); // for debug
  const chatId = message.chat.id;
  bot.sendMessage(chatId, 'Hello World');
