import org.telegram.telegrambots.api.methods.send.SendMessage;
import org.telegram.telegrambots.api.objects.Update;
import org.telegram.telegrambots.bots.TelegramLongPollingBot;
import org.telegram.telegrambots.exceptions.TelegramApiException;

public class MyFirstBot extends TelegramLongPollingBot {

	@Override
	public String getBotUsername() {
		// TODO Auto-generated method stub
		return "AlexrurBot";
	}

	@Override
	public void onUpdateReceived(Update update) {
		if(update.hasMessage()&&update.getMessage().hasText()){
			String message_text=update.getMessage().getText();
			long chat_id=update.getMessage().getChatId();
			SendMessage message=new SendMessage()
					.setChatId(chat_id)
					.setText(message_text);
			
			try{
				execute(message);
			} catch (TelegramApiException tel) {tel.printStackTrace();}
		}
	}

	@Override
	public String getBotToken() {
		// TODO Auto-generated method stub
		return "611477743:AAF9kAZqPP4U4ct3cVsdWvL_Y_YQlA94-hk";
	}

}
