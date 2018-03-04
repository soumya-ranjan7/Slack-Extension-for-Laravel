# A Laravel Package that makes Automatic Invitation to Slack Channels seamless


##  How it Works
After following all the information stated above, what next to do are:

**A)** Copy the code below to your `.env` file and make changes to the values.

```
SLACK_TEAM_NAME=
TEAM_DESCRIPTION=
SLACK_TEAM_URL=
SLACK_API_TOKEN=
SLACK_TEAM_EMAIL=

```

**Note:** Make sure you include the quotation mark.
> To get your Slack Api Token, check [https://api.slack.com/custom-integrations/legacy-tokens](https://api.slack.com/custom-integrations/legacy-tokens) and go to Legacy Token Generator to issue the token.

**B)** Copy the code below into your route file  `routes/web.php`

```
Route::get('/slack',[
    'uses'=>'LaravelSlackController@slackPage',
    'as'=>'slack'
]);

Route::post('/slack',[
    'uses'=>'LaravelSlackController@sendSlackInvite',
    'as'=>'slack'
]);

```

**C)** Use `php artisan serve` and check your slack invite page on `http://locahost:8000/slack
