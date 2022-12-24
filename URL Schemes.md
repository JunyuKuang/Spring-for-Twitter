
# URL Schemes

## TL;DR
Replace a Twitter URL's "https" prefix with "**spring**" to open the URL in Spring.

Replace a Mastodon URL's "https" prefix with "**mona**" to open the URL in Mona. 

For example: https://twitter.com/theSpringApp => spring://twitter.com/theSpringApp

## Preface

### Supported Schemes (URL Prefixes)
#### spring
Open one of these apps: Spring, Spring mini (version 4.3+), or Spring Beta.

#### mona
Open one of these apps: Mona, or Mona Beta.

#### Note
Use app ID as scheme if you have multiple editions of Spring installed.

Spring Beta: com.jonny.drift://

Spring: com.jonny.spring://

Spring mini: com.jonny.spring-lite://

Mona Beta: com.jonny.monabeta://

Mona: com.jonny.mona://

### Common Parameters
#### account
Perform a task with specific account identified by your Twitter handle (@username), or Mastodon user address. The value of account is case insensitive.

Twitter example: @theSpringApp
Mastodon example: @MonaApp@mastodon.social

## Switch Account
Provide "account" as parameter. Nothing changed if the target account is already activated on the current app window.

#### Examples:
spring://switch?account=@theSpringApp

mona://switch?account=@MonaApp@mastodon.social

## Open Tweet Composer
You can provide 2 optional parameters: text, account

The value of text parameter will be filled into the tweet composer view. If no account provided, Spring/Mona chooses a default account based on the current app window.

#### Examples:
spring://post?text=hello

mona://post?text=hello&account=@MonaApp@mastodon.social

## Open Search View
You can provide 2 optional parameters: text, account

The value of text parameter will be filled into the search bar.

### Examples:
spring://search?text=hello

mona://search?text=hello&account=@MonaApp@mastodon.social

## Open Twitter Links
Currently supports links to tweets (e.g. https://twitter.com/thespringapp/status/1344625888449556480), user pages (e.g. https://twitter.com/thespringapp), and Twitter Lists (e.g. https://twitter.com/i/lists/1344918930687729664)

## Open Mastodon Links
Supported formats:
User profile: https://[any_domain]/@[username]. https://mastodon.social/@MonaApp

Toot: https://[any_domain]/@[username]/[toot_id_number] https://mastodon.social/@MonaApp/109506252875971252

### Basic
Replace the “https” prefix in a Twitter URL with “spring”.

For example, open @theSpringApp’s user page using default account: 

spring://twitter.com/theSpringApp

### Advanced
Use the “open” URL scheme if you want to open multiple pages at once, or open a page with specific account.

The URL takes 2 parameters: url (required), and account (optional).

You may include multiple url parameters. "url" parameters must be percent encoded.

For example, open user page of @twitter and @jack with a signed in account called @theSpringApp would be something like this: 

spring://open?account=theSpringApp&url=https%3A%2F%2Ftwitter.com%2Ftwitter&url=https%3A%2F%2Ftwitter.com%2Fjack
