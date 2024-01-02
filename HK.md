import com.twilio.Twilio;
import com.twilio.converter.Promoter;
import com.twilio.rest.api.v2010.account.Message;
import com.twilio.type.PhoneNumber;

import java.net.URI;
import java.math.BigDecimal;

public class Example {
  // Find your Account Sid and Token at twilio.com/console
  public static final String ACCOUNT_SID = "AC9388f13e05ae3da13e2adc5f31a3ad13";
  public static final String AUTH_TOKEN = "[AuthToken]";

  public static void main(String[] args) {
    Twilio.init(ACCOUNT_SID, AUTH_TOKEN);
    Message message = Message.creator(
      new com.twilio.type.PhoneNumber("+2250748274816"),
      new com.twilio.type.PhoneNumber("+15407841563"),
      "Your message")
    .create();

    System.out.println(message.getSid());
  }
}
