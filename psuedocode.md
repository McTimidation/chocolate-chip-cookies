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

#### Arrays

allMix [
  largeBowl, whisk, woodSpat, spoon, plasWrap, smallBowl, bakingSoda.halfTea, salt.fullTea, vanilla.fullTea, sugar.halfCup, butter, brSugar.halfCup+brSugar.quarterCup, ssChunks.fullCup, darkChunks.fullCup, flour.fullCup+flour.quarterCup,
]

allBake [
  mitt, rack, scoop, bakeSheet, parchPaper,
]


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
  if (parameters > 2){
    container is last
  }
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

*cool*(){
  wait 5 min;
}

*eatCookies*(){
  eat cookies until sick
}

#### oven functions

*bake*(container, time){
  place container in oven for time;
  *beep*{
  make loud beep when bake time = 0
}
}

*off*(){
  turn off oven;
}


#### Primary function

*bakeCookies*(){

 *set*(allMix);

 *place*(butter, smallBowl);

 *microCook*(smallBowl, 30s);

 *place*(butter, sugar, brSugar, salt, largeBowl);

 *whisk*(largeBowl);

 *crack*(largeBowl);

 *place*(vanilla, largeBowl)

 *whisk*(largeBowl);

 *place(flour, bakingSoda, largeBowl);

 *fold*(largeBowl);

 *place*(ssChunks, darkChunks, largeBowl);

 *fold*(largeBowl);

 *cover*(largeBowl);

 *place*(largeBowl, fridge);

 *chill*();

 *set*(largeBowl);

 *uncover*();

 *set*(largeBowl, allBake);

 *place*(parchPaper, bakeSheet);

 *scoop*(largeBowl, parchPaper);


 if ( oven !== preheated){
  wait until preheated;
 } else { *place*(bakesheet, oven);
  bake(bakeSheet, 12min)
  }

if (beep = true){
  *place.mitt*(bakeSheet, rack);
  *cool*();
 }
}

### Procedural code

if (wantCookies = true){
  bakeCookies();
  eatCookies();
} else {
  code
}












