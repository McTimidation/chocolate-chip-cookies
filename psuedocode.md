# Formula for Chocolate Chip Cookies

### Variables for tools and containers


largeBowl = Large Mixing Bowl
-container for mixing

whisk = Whisk
- tool for lite mixing

woodSpat = Wooden Spatula
- tool for folding

spoon = Large spoon
- tool for heavy mixing

bakeSheet = Baking Sheet
- container for baking

parchPaper = Parchment Paper 
- tool to place over Baking Sheet

oven = Oven
- tool for baking 

fridge = Refridgerator
- tool for chilling

plasWrap = Plastic wrap for large bowl
- tool to cover large bowl

smallBowl = Small bowl
- container to melt butter

mitt = Oven Mitt
- tool to grab hot pan

counter = Kitchen Counter 
- container for containers

rack = Cooling Rack
-container for hot baking sheet

microWave = Microwave Oven
- tool to heat containers 

halfTea = 1/2 teaspoon 
- tool for measuring

fullTea = 1 teaspoon
- tool for measuring

halfCup = 1/2 cup
- tool for measuring

fullCup = 1 Cup
- tool for measuring

quarterCup = 1/4 Cup
- tool for measuring

scoop = ice cream scoop
- tool for scooping dough


#### Variables for Ingredients

ingredient.tool = to be used with a measuring device

bakingSoda = Baking Soda

salt = Table salt

vanilla = Vanilla Extract

sugar = White Sugar

butter = 1 stick unsalted butter

brSugar = Brown Sugar

ssChunks = Semi-Sweet Chocolate Chunks
darkChunks = dark chocolate chunks

flour = all purpose flour

### Property variables
smooth = no lumps

mixed = all ingredients well incorporated

temp = temperature in degrees fahrenheit

preheated = oven has reached preheat temp

empty = contents of container are < %2

hot = too hot to touch

wantCookies = I want cookies

### Functions


*set*(variable){
  move variable from current location to *counter*
}

*place*(variable, container){
  } move variable from current location to container
  

*microCook*(container, time){
microwave container for time
}

*whisk*(container){
  lightly mix contents of container with whisk until mixed
}

*crack*(container){
  lightly break shell of egg and pour contents into container
}

*fold*(container){
  mix contents of container with wooden spoon until mixed
}

*mix*(container){
  mix contents of container until mixed
}

*cover*(container){
  place plasWrap over container
}

*uncover*{
  remove plasWrap from container and discard
}

*chill*(){
  leave for 6 hours
}

*preheat*(temp){
  set oven to temp
}

*scoop*(container, container){
  use scoop to place contents of container1 onto container2
}

*bake*(container, time){
  place container in oven for time
}
#### oven functions
*beep*{
  make loud beep for 30 seconds
}

#### Primary function

*bakeCookies*(){

}

### Procedural code

if (wantCookies = true){
  bakeCookies();
}












