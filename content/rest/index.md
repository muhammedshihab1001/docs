def music_free(update: Update, context: CallbackContext):
 try:
  if "#musicafree" in update.message.text.partition(' ')[0]:
   bot.send_message(-1001368024147,update.message.text.partition(' ')[2])
  else:
   pass
 except:
  pass
musica_handler= MessageHandler(Filters.text & (~Filters.command), music_free)
 dispatcher.add_handler(musica_handler)
 dispatcher.add_handler(CallbackQueryHandler(button))
