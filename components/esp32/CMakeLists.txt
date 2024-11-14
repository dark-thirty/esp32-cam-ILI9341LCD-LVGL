#IDF version is less than IDF5.0
idf_component_register(
    SRCS "esp32.c" ${SRC_VER}
    INCLUDE_DIRS "include"
    PRIV_INCLUDE_DIRS "priv_include"
    REQUIRES driver spiffs
    PRIV_REQUIRES fatfs esp_lcd esp_lcd_ili9341
)
