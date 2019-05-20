# Wikipedia-Viewer

*Displays Wikipedia Results*

This is an app that allows you to view Wikipedia documents linked to a specific search term entered by the user.


...

**Home Page**

<img src="/WikipediaViewer.PNG" title="home page" alt="home page" width="500px">


---


## Table of Contents 

> Sections
- [Sample Code](#Sample_Code)
- [Installation](#installation)
- [Features](#features)
- [Contributing](#contributing)
- [Team](#team)
- [FAQ](#faq)
- [Support](#support)
- [License](#license)


---

## Sample Code

```javascript
// code

  var url="https://en.wikipedia.org/w/api.php?action=opensearch&limit=10&namespace=0&format=json&search=";
  var input= document.getElementById('minutely').value;
  
  var ajax1= $.ajax({url:url+input+'&callback=JSON_CALLBACK',
          type: 'GET',
          dataType:'jsonp',
          headers: {'Api-User-Agent': 'WikiViewer/1.0'}
  }); 
          
  $.when(ajax1).done(  
    function(data){
      for(var i=0; i< data[1].length; i++){
        $('#response'+i).html("<a href='"+data[3][i] +"'>"+data[1][i]+"</a>")
        $('#response2'+i).html(data[2][i])
        $('.box').css('width', '500px')
        //$('.box').css('left', '-50%')
        $('.box').css('display', 'block')
              
        $('#inside').css('position', 'relative')
        $('#inside').css('transform', 'translate(-50%,0%)')
        $('#inside').css('top', '0%')
              
     }
  })
  
```

---

## Installation

## Features
## Usage (Optional)
## Documentation (Optional)
## Tests (Optional)
## Contributing
## Team

> Contributors/People

| [**seansangh**](https://github.com/seansangh) |
| :---: |
| [![seansangh](https://avatars0.githubusercontent.com/u/45724640?v=3&s=200)](https://github.com/seansangh)    |
| [`github.com/seansangh`](https://github.com/seansangh) | 

-  GitHub user profile

---

## FAQ

- **Have any *specific* questions?**
    - Use the information provided under *Support* for answers

---

## Support

Reach out to me at one of the following places!

- Twitter at [`@sean13nay`](https://twitter.com/sean13nay?lang=en)
- Github at [`seansangh`](https://github.com/seansangh)

---

## Donations (Optional)

- If you appreciate the code provided herein, feel free to donate to the author via [Paypal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=4VED5H2K8Z4TU&source=url).

[<img src="https://www.paypalobjects.com/webstatic/en_US/i/buttons/cc-badges-ppppcmcvdam.png" alt="Pay with PayPal, PayPal Credit or any major credit card" />](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=4VED5H2K8Z4TU&source=url)

---

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
- Copyright 2019 © <a>S.S.</a>
