# shopify-google-location-map-with-api
HTML code — Add Google Map
It’s a simple HTML code.  The Google Map will be visible within the below-mentioned div.

<div id="google_map"></div>
The first things you will need is the latitude and longitude of the location. You can easily get it from the Google Map website. Type your search location and enter. Then mark the exact location. A marker will appear and display your latitude and longitude coordinates.

JavaScript code
Now initialize the variable latlng with these coordinates. options variable holds different types of attributes. You can change the attribute value according to your need. And last marker variable set the marker to the Google Map.

<script type="text/javascript">
function initiateGoogleMap() {
  
  //Latlng variable containing the coordinate for the center of the map
  var latlng = {lat:25.200134, lng:77.982206};
      
  //Some properties we want to pass to the map  
  var options = {  
    zoom: 4, //The initial zoom level of the map
    center: latlng, //The map centered based on the coordinates
    mapTypeId: google.maps.MapTypeId.ROADMAP //All map types are -- ROADMAP/SATELLITE/HYBRID/TERRAIN
  }; 
 
  //Initializing the map  
  var map = new google.maps.Map(document.getElementById('google_map'), options);  
    
  //Add Marker to the map
  var marker = new google.maps.Marker({
    position: latlng, 
    map: map    
  });  
}
</script>
The last thing you need to add to your script that is the Google Maps API —

</script>
  <script async defer src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initiateGoogleMap">
</script>
One API key is required to display the Google Map. You can get your API key from Google Maps APIs.

Complete code — Add Google Map
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" />
<title>Add Google Map with a marker to your website</title>
<style>
body { font-family:Arial, Helvetica, sans-serif; font-size:14px; }
h1 { clear:both; margin-bottom:30px; font-size:17px; }
h1 a { font-weight:bold; color:#0099FF; }
span { clear:both; display:block; margin-bottom:30px; }
span a { font-weight:bold; color:#0099FF; }
#google_map { width:100%; height:500px; border:1px dashed #000; }
</style>
</head>
<body>
  <div class="contentDiv">
    <h1>Read the full article -- <a href="http://www.mitrajit.com/2016/12/add-google-map-marker-website/" target="_blank">Add Google Maps with a marker to your website</a> in Mitrajit's Tech Blog</h1>
  
    <div id="google_map"></div>
  </div><!-- end of .contentDiv -->
  <script type="text/javascript">
  function initiateGoogleMap() {
  
      //Latlng variable containing the coordinate for the center of the map
      var latlng = {lat:25.200134, lng:77.982206};
      
      //Some properties we want to pass to the map  
      var options = {  
         zoom: 4, //The initial zoom level of the map
         center: latlng, //The map centered based on the coordinates
         mapTypeId: google.maps.MapTypeId.ROADMAP //All map types are -- ROADMAP/SATELLITE/HYBRID/TERRAIN
      }; 
 
      //Initializing the map  
      var map = new google.maps.Map(document.getElementById('google_map'), options);  
    
      //Add Marker to the map
      var marker = new google.maps.Marker({
         position: latlng, 
         map: map    
      });  
}
</script>
<script async defer src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initiateGoogleMap">
</script>
</body>
</html>
You can download the complete source code from the below download link and please like and share the tutorial link to others.
