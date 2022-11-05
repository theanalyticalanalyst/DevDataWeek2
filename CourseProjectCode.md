new_icon <- awesomeIcons(
  icon = 'ios-close',
  iconColor = 'black',
  library = 'ion',
  markerColor = "red"
)

content <- paste(sep = "<br/>",
  "<b>ICICI BANK</b>",
  "Kunal Icon Rd",
  "Pune, 411027"
)

my_map <- leaflet() %>%
    addTiles() %>%
    addAwesomeMarkers(lat = 18.593470, lng = 73.795123,
        icon = new_icon,
        popup = "Good Coffee at the local CCD") %>%
    addPopups(lat = 18.593417, lng = 73.795595, content,
        options = popupOptions(closeButton = FALSE)
    )
my_map
