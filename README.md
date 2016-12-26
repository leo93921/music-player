# music-player

##What's this?
This is an html5 music player that works using jPlayer.
It's derived from the Codebase music player (http://www.codebasehero.com/2011/07/html5-music-player-updated)
and it's designed to be minimal.
Here it is a screenshot:
![Alt text](screenshot.gif?raw=true "Screenshot")

##How to use it
You can use it by adding in the head section of your document:
```html
    <link rel="stylesheet" type="text/css" href="path_to_plugin/css/ttw-music-player.css">
    <script type="text/javascript" src="js/jquery-1.6.1.min.js"></script>
    <script type="text/javascript" src="path_to_plugin/jquery-jplayer/jquery.jplayer.js"></script>
    <script type="text/javascript" src="path_to_plugin/ttw-music-player.js"></script>
```

After that, you have to add a div with a class or an id that you will use to initialize the plugin.
Suppose you want to write the div in the following way:
```html
    <div id="audio-player"></div>
```

Now you can use the following sample to initialize the plugin:
```javascript
    <script type="text/javascript">
        $(document).ready(function(){
            var description = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce id tortor nisi. Aenean sodales diam ac lacus elementum scelerisque. Suspendisse a dui vitae lacus faucibus venenatis vel id nisl. Proin orci ante, ultricies nec interdum at, iaculis venenatis nulla. ';
            var myPlaylist = [{
                mp3:'mix/1.mp3',
                oga:'mix/1.ogg',
                title:'Track Title',
                artist:'Artist Name',
                rating:4,
                buy:'#',
                price:'0.99',
                duration:'0:30',
                cover:'mix/1.jpg'
            }]
  
            $('#audio-player').ttwMusicPlayer(myPlaylist, {
                autoPlay:false,
                description:description,
                jPlayer:{
                    swfPath:'../plugin/jquery-jplayer' //You need to override the default swf path any time the directory structure changes
                }
            });
        });
    </script>
```
If you want to add more than one item in the tracklist, you need to add these files in the myPlaylist javascript variable.
An example of multi-item playlist:
```javascript
  var myPlaylist = [
    {
      mp3:'mix/1.mp3',
      oga:'mix/1.ogg',
      title:'Track Title',
      artist:'Artist Name',
      rating:4,
      buy:'#',
      price:'0.99',
      duration:'0:30',
      cover:'mix/1.jpg'
    },
    {
      mp3:'mix/1.mp3',
      oga:'mix/1.ogg',
      title:'Track Title',
      artist:'Artist Name',
      rating:4,
      buy:'#',
      price:'0.99',
      duration:'0:30',
      cover:'mix/1.jpg'
    }
  ]
```
Once you have done this, you should see the plugin loaded.



