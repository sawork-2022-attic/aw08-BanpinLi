# aw08

#### 1、访问更加方便。

在没有进行集成的时候，由于delivery是一个独立的系统，访问delivery使用的ip+port和访问micropos使用的ip+port是不一样的，所以对于外界访问的用于而言，需要自己掌握这些差距并按照规定进行正确的访问，这对于外界用户访问而言是不友好的，Integration的作用就是将delivery的功能整合到micropos中，能够使得外界用户可以在保持ip+port不变的情况下访问到delivery的资源，

#### 2、方便指定访问的策略

delivery这个独立的系统对外界是提供了一套可供访问的api，如果我们想要在外界通过不同的访问方式来访问一个api的话，在未进行集成的时候，可能需要去修改delivery的相关接口；但是使用Integration进行应用集成之后，在进行集成的中间层面，我们就可以很方便的指定各种api的访问的方式，新增或修改访问的方式，使得我们可以在不修改第三方系统的前提下，可以在外界以另一种方式访问某一种功能。



---

Run the project with `mvn spring-boot:run` and send request to `http://localhost:8080/check`. You should see an reponses in json format like the following.

```json
{
    "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
    "id": "kswv7NIaTCaIIErlBzODaA",
    "url": "https://api.chucknorris.io/jokes/kswv7NIaTCaIIErlBzODaA",
    "value": "Chuck Norris's shadow weighs 250 pounds and can kick your ass ."
}
```

Try to understand the provided code which demonstrates spring integration between a spring boot application with an externel http service (https://api.chucknorris.io/jokes/random).

Please implement delivery as an standalone service (just like the random joke service). Refer the sample code to integrate your Micropos system with delivery service so that user can check delivery status on Miropos which actually forwards user request to delivery service on demand.

![](Micropos.svg)

Consider the advantage by doing so and write it down in your readme file.
