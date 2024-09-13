const { Telegraf } = require("telegraf");

// Botni yaratish
const bot = new Telegraf("sizning tokiningiz");

// /start komandasi uchun handler
bot.command("start", (ctx) => {
  const { first_name, last_name } = ctx.message.from;
  const fullName = `${first_name || ""} ${last_name || ""}`.trim();

  ctx.reply(
    `Salom, ${
      fullName || "Mehmon"
    }! Botga xush kelibsiz botni ishlatish uchun amallar kiriting. `,
    {
      reply_markup: {
        keyboard: [[{ text: "Havolalar" }]],
        resize_keyboard: true,
        one_time_keyboard: true,
      },
    },
  );
});
bot.command("history", (ctx) => {
  const userId = ctx.message.from.id;

  if (userMathExpressions.has(userId)) {
    const expressions = userMathExpressions.get(userId);
    const historyText = expressions
      .map((expr, index) => `${index + 1}. ${expr.command} = ${expr.result}`)
      .join("\n");
    ctx.reply(`Sizning avvalgi matematik amallaringiz:\n${historyText}`);
  } else {
    ctx.reply("Siz hali matematik amal qilmagansiz.");
  }
});

// Keyboard tugmisi bosilganda ishlaydigan handler
bot.hears("Havolalar", (ctx) => {
  ctx.reply("BIZNING ASOSIY SINF BOTMIZ HAMDA GURUHIMIZ", {
    reply_markup: {
      inline_keyboard: [
        [
          { text: "nom", url: "lik" },
          { text: "nom", url: "link" },
        ],
      ],
    },
  });
});

// Foydalanuvchilar matematik amallarini saqlash uchun ma'lumotlar bazasi

bot.command("cl", (ctx) => {
  const userId = ctx.message.from.id;
  const chatId = ctx.chat.id;
  const command = ctx.message.text.slice(4).trim();

  try {
    const result = eval(command);

    // Foydalanuvchi uchun amalni saqlash
    if (!userMathExpressions.has(userId)) {
      userMathExpressions.set(userId, []);
    }
    userMathExpressions.get(userId).push({ command, result });

    // Guruhga yuborish
    bot.telegram.sendMessage(chatId, `Natija: ${command} = ${result}`);
  } catch (error) {
    ctx.reply("Xatolik yuz berdi. Iltimos, to'g'rlab yozing.");
  }
});
const userMathExpressions = new Map();
bot.on("text", (ctx) => {
  const input = ctx.message.text;
  try {
    const result = eval(input); // Ixtiyoriy to'g'ridan-to'g'ri natijani olish uchun eval() funksiyasidan foydalanamiz
    ctx.reply(`Natija: ${input} = ${result}`);
  } catch (error) {
    ctx.reply("Xatolik yuz berdi. Iltimos, to'g'rlab yozing.");
  }
});

// Foydalanuvchi uchun avvalgi matematik amallarini chiqarish uchun handler

// Botni ishga tushirish
bot.launch();
