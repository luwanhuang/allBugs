```
imports: [
    MailgunModule.forAsyncRoot({
      inject: [ApiConfigService],
      useFactory: async (configService: ApiConfigService) => {
        return {
          DOMAIN: configService.mailGunConfig.domain,
          API_KEY: configService.mailGunConfig.apiKey,
          // HOST: 'www.checkit.com', // default: 'api.mailgun.net'. Note that if you are using the EU region the host should be set to 'api.eu.mailgun.net'
        };
      },
    }),
  ],
 ```
 do inject when you want use async configuration. 
ApiProperty cannot use type: Enum, use enum: Enum
