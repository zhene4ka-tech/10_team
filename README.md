
### Датасет содержит:
1. Твиты собственников и топ-менеджеров компаний, государственных деятелей.
2. Котировки акций и курсов валют.
3. Сопоставление твитов и изменений котировок.

### Датасет предназначен для исследования влияния словесных интервенций на котировки.

### По котировкам и акциям взяты следующие данные:

1. Курс фунта стерлингов к доллару, к евро, рублю. Источник: официальные данные банка Англии https://www.bankofengland.co.uk/
2. Курс евро к доллару. Источник: официальные данные ЕЦБ https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/usd.xml
3. Курс шекеля к евро и доллару. Источник: официальные данные банка Израиля https://www.boi.org.il/en/Markets/ExchangeRates/Pages/Default.aspx
4. Акции Microsoft, Tesla, Apple, TCSG, Alibaba, Dell, Alphabet. Источник: NASDAQ, Yahoo Finance https://finance.yahoo.com/
5. Акции Virgin America, Virgin Australia, Virgin Galactic. Источники: NASDAQ, ASX, NYSE Investing.com
  https://www.investing.com/equities/virgin-america-inc-historical-data  
  https://www.investing.com/equities/virgin-australia-historical-data  
  https://www.investing.com/equities/social-capital-hedosophia-historical-data  

### Твиты собраны по следующим персоналиям:

###### US Business leaders

Jeff Weiner- LinkedIn @jeffweiner Joined February 2009    
Tim Cook- Apple @tim_cook Joined July 2013    
Bill Gates- Microsoft @BillGates Joined June 2009   
Michael Dell- Dell @MichaelDell Joined July 2009   
Mary Barra- GM @mtbarra Joined February 2013    
Warren Buffett- Berkshire Hathaway @WarrenBuffett Joined April 2013  
Sundar Pichai- Google @sundarpichai CEO, Google and Alphabet Joined March 2008    

###### Asia/China
Jack Ma Founder of AlibabaGroup @JackMa Joined March 2020  
Ma Huateng @ma_tencent CEO of Tencent Holdings Limited Joined September 2017

###### European politicians

Emmanuel Macron France @EmmanuelMacron Joined October 2013  
Theresa May UK @theresa_may Joined June 2016  
Benjamin Netanyahu @netanyahu Prime Minister of Israel Joined October 2008  
Reuven Rivlin @PresidentRuvi live updates from the 10th President of the State of Israel - Joined November 2014  

###### Russian business leader

Oleg Tikov @olegtinkov Joined April 2009


### Структура датасета:

``` 
/
|___merge_data.py
|___merging_custom_function.py
|
|__/People
|  |
|  |__/elon_musk
|  |  |__elon_musk.json
|  |  |__elon_musk.txt
|  |  
|  |__/bill_gates
|  |  |__bill_gates.json
|  |  |__bill_gates.txt
|  |
|  |__/...
|   
|__/Assets
|  |  
|  |__/Microsoft
|  |  |__microsoft_1986_2020.csv
|  |
|  |__/Tesla
|  |  |__tesla_2010_2020.csv
|  |
|  |__/...
|
|__/People_vs_Assets
   |
   |__/gates_microsoft
   |  |__gates_microsoft.csv
   |  |__MSFT_Close_vs_Gates_tweets.jpg
   |
   |__/musk_tesla
   |  |__musk_tesla.csv
   |  |__TSLA_Close_vs_Musk_tweets.jpg
   |
   |__/...
 ```

### Структура json-файла твитов:

``` 
{'2020-10-19 00:32:08': 
  {'contributors': None,
   'coordinates': None,
   'created_at': 'Mon Oct 19 00:32:08 +0000 2020',
   'entities': {'hashtags': [],
              'media': [{'display_url': 'pic.twitter.com/Gy9a20uMmX',
                         'expanded_url': 'https://twitter.com/elonmusk/status/1317986858983321600/photo/1',
                         'id': 1317986854340186112,
                         'id_str': '1317986854340186112',
                         'indices': [42, 65],
                         'media_url': 'http://pbs.twimg.com/media/EkpuD5-U0AA899g.jpg',
                         'media_url_https': 'https://pbs.twimg.com/media/EkpuD5-U0AA899g.jpg',
                         'sizes': {'large': {'h': 1110,
                                             'resize': 'fit',
                                             'w': 1124},
                                   'medium': {'h': 1110,
                                              'resize': 'fit',
                                              'w': 1124},
                                   'small': {'h': 672,
                                             'resize': 'fit',
                                             'w': 680},
                                   'thumb': {'h': 150,
                                             'resize': 'crop',
                                             'w': 150}},
                         'type': 'photo',
                         'url': 'https://t.co/Gy9a20uMmX'}],
              'symbols': [],
              'urls': [],
              'user_mentions': [{'id': 18809812,
                                 'id_str': '18809812',
                                 'indices': [0, 12],
                                 'name': 'Toby Young',
                                 'screen_name': 'toadmeister'}]},
 'extended_entities': {'media': [{'display_url': 'pic.twitter.com/Gy9a20uMmX',
                                  'expanded_url': 'https://twitter.com/elonmusk/status/1317986858983321600/photo/1',
                                  'id': 1317986854340186112,
                                  'id_str': '1317986854340186112',
                                  'indices': [42, 65],
                                  'media_url': 'http://pbs.twimg.com/media/EkpuD5-U0AA899g.jpg',
                                  'media_url_https': 'https://pbs.twimg.com/media/EkpuD5-U0AA899g.jpg',
                                  'sizes': {'large': {'h': 1110,
                                                      'resize': 'fit',
                                                      'w': 1124},
                                            'medium': {'h': 1110,
                                                       'resize': 'fit',
                                                       'w': 1124},
                                            'small': {'h': 672,
                                                      'resize': 'fit',
                                                      'w': 680},
                                            'thumb': {'h': 150,
                                                      'resize': 'crop',
                                                      'w': 150}},
                                  'type': 'photo',
                                  'url': 'https://t.co/Gy9a20uMmX'}]},
 'favorite_count': 3018,
 'favorited': False,
 'geo': None,
 'id': 1317986858983321600,
 'id_str': '1317986858983321600',
 'in_reply_to_screen_name': 'elonmusk',
 'in_reply_to_status_id': 1315052624748535808,
 'in_reply_to_status_id_str': '1315052624748535808',
 'in_reply_to_user_id': 44196397,
 'in_reply_to_user_id_str': '44196397',
 'is_quote_status': False,
 'lang': 'tl',
 'place': None,
 'possibly_sensitive': False,
 'retweet_count': 925,
 'retweeted': False,
 'source': '<a href="http://twitter.com/download/iphone" '
           'rel="nofollow">Twitter for iPhone</a>',
 'text': '@toadmeister Sweden at zero deaths Oct 15 https://t.co/Gy9a20uMmX',
 'truncated': False,
 'user': {'contributors_enabled': False,
          'created_at': 'Tue Jun 02 20:12:29 +0000 2009',
          'default_profile': False,
          'default_profile_image': False,
          'description': '',
          'entities': {'description': {'urls': []}},
          'favourites_count': 6929,
          'follow_request_sent': False,
          'followers_count': 39446809,
          'following': True,
          'friends_count': 97,
          'geo_enabled': False,
          'has_extended_profile': True,
          'id': 44196397,
          'id_str': '44196397',
          'is_translation_enabled': False,
          'is_translator': False,
          'lang': None,
          'listed_count': 56487,
          'location': '',
          'name': 'Elon Musk',
          'notifications': False,
          'profile_background_color': 'C0DEED',
          'profile_background_image_url': 'http://abs.twimg.com/images/themes/theme1/bg.png',
          'profile_background_image_url_https': 'https://abs.twimg.com/images/themes/theme1/bg.png',
          'profile_background_tile': False,
          'profile_banner_url': 'https://pbs.twimg.com/profile_banners/44196397/1576183471',
          'profile_image_url': 'http://pbs.twimg.com/profile_images/1295975423654977537/dHw9JcrK_normal.jpg',
          'profile_image_url_https': 'https://pbs.twimg.com/profile_images/1295975423654977537/dHw9JcrK_normal.jpg',
          'profile_link_color': '0084B4',
          'profile_sidebar_border_color': 'C0DEED',
          'profile_sidebar_fill_color': 'DDEEF6',
          'profile_text_color': '333333',
          'profile_use_background_image': True,
          'protected': False,
          'screen_name': 'elonmusk',
          'statuses_count': 12639,
          'time_zone': None,
          'translator_type': 'none',
          'url': None,
          'utc_offset': None,
          'verified': True}}
}
 ```




### Наименования столбцов csv-файлов котировок:
Date, Open_TICKER, High_TICKER, Low_TICKER, Close_TICKER, Volume_TICKER
### Наименования столбцов csv-файлов курсов валют:
Date, Currency_name
### Наименования столбцов csv-файла сводной таблицы::
Date, Name, Tweets, Open_TICKER, High_TICKER, Low_TICKER, Close_TICKER, Volume_TICKER
 

