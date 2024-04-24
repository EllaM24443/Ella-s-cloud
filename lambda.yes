import { SESClient, SendEmailCommand } from "@aws-sdk/client-ses";
const ses = new SESClient({ region: "us-east-2" });

export const handler = async(event,context) => {
  const command = new SendEmailCommand({
    Destination: {
      ToAddresses: ["EGMergy01@indianatech.net"],
    },
    Message: {
      Body: {
        Text: { Data: "This is a sample email from the AWS SES Lambda" },
      },

      Subject: { Data: "NET1500 2024 AWS Lambda Test Email" },
    },
    Source: "EGMergy01@indianatech.net",
  });

  try {
    let response = await ses.send(command);
    return response;
  }
  catch (error) {
    console.log(error);
  }
  finally {
  }
};