# WorkCompass OmniAuth Google OAuth2 Strategy

Strategy to authenticate with Google via OAuth2 in OmniAuth. Fork from [zquestz/omniauth-google-oauth2](https://github.com/zquestz/omniauth-google-oauth2) version 0.6.0.

# Derivation

## Custom Google Domain

This has been fork from the original gem to allow setting custom Google Domain in order to allow developers to test locally.

### Usage

```
Rails.application.config.middleware.use OmniAuth::Builder do
  provider :google_oauth2, ENV['GOOGLE_CLIENT_ID'], ENV['GOOGLE_CLIENT_SECRET'], client_options: {
    site => 'https://oauth2.example.com',
    authorize_url => 'https://accounts.example.com/o/oauth2/auth',
    base_api_url => 'https://www.example.com',
    base_auth_domain => 'accounts.example.com'
  }
end
```

## DevContainer

Also include setup to run into VSCode devcontainer to contribute to this project.
