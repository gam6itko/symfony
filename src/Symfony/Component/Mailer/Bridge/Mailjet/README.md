Mailjet Bridge
==============

Provides Mailjet integration for Symfony Mailer.

Configuration examples:

```dotenv
# API
MAILER_DSN=mailjet+api://$PUBLIC_KEY:$PRIVATE_KEY@default
# SMTP
MAILER_DSN=mailjet+smtp://$PUBLIC_KEY:$PRIVATE_KEY@default
```

Custom headers
--------------

Api transport converts headers below to certain message properties.

```php
$email->getHeaders()
    // TemplateLanguage
    ->addTextHeader('X-MJ-TemplateLanguage', true)
    // TemplateID
    ->addTextHeader('X-MJ-TemplateID', '12345')
    // TemplateErrorReporting
    ->addTextHeader('X-MJ-TemplateErrorReporting', 'errors@mailjet.com')
    // TemplateErrorDeliver
    ->addTextHeader('X-MJ-TemplateErrorDeliver', true)
    // Variables
    ->addTextHeader('X-MJ-Vars', '{"varname1": "value1","varname2": "value2", "varname3": "value3"}')
    // CustomID
    ->addTextHeader('X-MJ-CustomID', 'CustomValue')
    // EventPayload
    ->addTextHeader('X-MJ-EventPayload', 'Eticket,1234,row,15,seat,B')
    // CustomCampaign
    ->addTextHeader('X-Mailjet-Campaign', 'SendAPI_campaign')
    // DeduplicateCampaign
    ->addTextHeader('X-Mailjet-DeduplicateCampaign', true)
    // Priority
    ->addTextHeader('X-Mailjet-Prio', 2)
    // TrackClick
    ->addTextHeader('X-Mailjet-TrackClick', "account_default")
    // TrackOpen
    ->addTextHeader('X-Mailjet-TrackOpen', "account_default");
```

Resources
---------

 * [Contributing](https://symfony.com/doc/current/contributing/index.html)
 * [Report issues](https://github.com/symfony/symfony/issues) and
   [send Pull Requests](https://github.com/symfony/symfony/pulls)
   in the [main Symfony repository](https://github.com/symfony/symfony)
