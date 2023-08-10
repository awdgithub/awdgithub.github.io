<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>The Schnaldridge School for Leadership and International Studies</title>
    <link rel="stylesheet" href="styles.css" />
    <h1>The Schnaldridge School for Leadership and International Studies</h1>
    <h2>where girls change the world</h2>
  </head>
  <body>
    <nav>
      <a href="#index">Home</a>
      <a href="#country">Country</a>
      <a href="#capital">Capital</a>
      <a href="#weather">Weather</a>
    </nav>
    <div id="country">
      <input type="name" name="country" id="countryname" />
      <py-script>
        import requests
        from bs4 import BeautifulSoup

        response = requests.get("https://en.wikipedia.org/wiki/Ghana")
        soup = BeautifulSoup(response.content, 'html.parser')

        data = []
        table = soup.find("table", class_="infobox ib-country vcard")
        table_body = table.find('tbody')
        
        images = table_body.findAll('img')
        flag = images[0]
        flag.attrs['src']
      </py-script>
    </div>
    <div id="capital">
      <p>The capital of <a id="countryname"></a> is 
      </p>
    </div>
    <div id="weather">
    </div>
  </body>
</html>
