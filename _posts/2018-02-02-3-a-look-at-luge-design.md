---
layout: post
title: 3. a look at luge design
date: 2018-02-02 18:33
author: iuyhcdfs
comments: true
categories: [design, luge]
---
[caption id="attachment_161" align="aligncenter" width="626"]<img class="alignnone  wp-image-161" src="https://iuondesign.files.wordpress.com/2018/02/qtownlugecropped.png" alt="qtownlugecropped" width="626" height="293" /> A shot from the chairlift.[/caption]
<p style="text-align:center;"><em><strong>the "Luge" is basically gravity-powered go-karts.
</strong></em>Being on holiday wont stop me analyzing the last "game" I played
<!--more--></p>
&nbsp;
<p style="text-align:center;"><a href="#whatsaluge">Whats a Luge</a> &gt; <a href="#thedesign">The Design</a> &gt; <a href="#driversnotes">Drivers Notes</a> &gt; <a href="#closing">Closing</a></p>
<p style="text-align:center;"><em>This is perhaps the only time I'll talk about strong design constraints.
Fortunately, we don't have real-life consequences in video games (wait maybe we do).</em></p>
<a name="whatsaluge"></a>

&nbsp;
<h2><strong>whats a luge?</strong></h2>
You ride the "Luge" vehicle down a hillside track. You sit in a strong plastic seat which is elongated like a go-kart, but without any engine or chassis sticking out the sides.

In front of you appears to be like a bicycle handlebar, which you will turn to steer. The steering available is also more intuitive than a bicycle: if you <em>don't</em> lean your body in the direction you're turning, you'll stay in control.

But the Luge isn't moving yet.

If you pull the whole handlebar towards you a little (like a lever), you'll let the front wheels touch the ground and you'll start moving.

If you pull the whole handlebar even further, you actually start engaging some brakes to slow you down.

That's all.

While the controls are weird, the appeal of this attraction is obvious as an unfamiliar vehicle ride that you have control over. Any unfamiliar activity has the potential satisfaction once you learn it, as long as it lets you learn how to drive comfortably.

You also get to feel the wind and look at nice scenery.

Given that there is appeal, lets see what there is to design.

<a name="thedesign"></a>

&nbsp;
<h2><strong>the design: three big goals</strong></h2>
<strong>The vehicle is always the same design.</strong> The one used in New Zealand is identical to the one used in Singapore.

What we're going to talk about is the level design, the sloped tracks!

The Luge has other requirements to fulfill. The main ones, that NEED our focus boil down to:
<ul>
	<li>Safety</li>
	<li>Challenge</li>
	<li>Variety</li>
</ul>
<strong>Safety is priority one... since it's not a videogame. </strong>Crash pads, slow signs, short or tall walls all exist or else you're out of business.

The track happens to decide your Luge's capabilities. The steepness of your track can decide the maximum acceleration AND the maximum speed. On the advanced track, short moments of steep slopes are sparingly used just enough to provide a slight "loss of control" thrill feeling.

<strong>Challenge, or provoke the use of steering and braking. </strong>It's about placing turns. Slight or sharp curvatures, and also giving drivers a runway to speedup before asking them to slow before a turn.

You are secretly able to take the majority of the course at full throttle, but <strong>only</strong><strong> if you can use the</strong> <strong>untold</strong><strong> technique</strong> of leaning your own body in the direction you steer.

It's not easy to lean and steer at the same time while also pulling the handlebar to continue accelerating, so many drivers also won't take corners at top speed anyway.

If we're talking about flow, the Luge has an interesting dilemma.

<strong>Variety is your chief tool against boredom.</strong> You have limited hillside to work with, and limited replay value with a single track.

You can then... add more tracks. At the Sentosa Luge in Singapore a few years back, I recall only one track, and it was very much (or could have used to be) a road for two cars with physical obstacles.

At the Queenstown Luge, there are 2 tracks, both of which would only be wide enough to fit a single car. You have to drive on the "Scenic" blue route once before you can attempt the red route (which is potentially dangerous for fearful first-time drivers).

The tradeoff between the track width is: Sentosa can mix up physical obstacles to steer around while Queenstown gains variety simply from more tracks. Having an experienced track also allows drivers more acclimated to speed still enjoy the luge without being blocked by beginners on a thin road.

Here's a hastily shot picture of the routes (the left part got cropped but the red and blue tracks only crossover that one time in the middle)

<img class="  wp-image-162 aligncenter" src="https://iuondesign.files.wordpress.com/2018/02/luge-map-e1517543114642.jpg" alt="luge map" width="391" height="328" />

Intriguingly, if you look at the shadows and contours of the mountain, the hardest thing to build is a straightway! The twists and turns were basically decided by the mountain. All your company needs to do is make a downhill course <em>safe</em>, and it'll be exciting.

<a name="driversnotes"></a>

&nbsp;
<h2><strong>driver's notes: results of playtesting</strong></h2>
It's hard to really explain any further without letting you drive it, but should you want to consider designing one in the future:

1: Chicanes (snake-like paths that require drivers to repeatedly steer left-right-left-right) are always the most fun sections <strong>for the vehicle you have</strong>, as it takes advantage of the luge's responsive handlebar steering and exposes you to how much control you truly have.

Corners that can be cut are also very interesting, and when going downhill, can only safely exist on a chicane.

2: Its good that the vehicle cannot drift. In a car, both engine acceleration and braking can be used to control your drift. In the Luge, you do not have an engine, and only braking exists. Also beginners who accidentally enters a drift are probably in trouble.

3: The wider road at Sentosa Luge gives much more room to overtake compared to Queenstown. Speeding and overtaking doesn't appeal to everyone however. You can still however, place crash barriers along a wide road to create a chicane.

4: The control is not completely intuitive. When you engage the wheels by pulling the handlebar: If you don't pull, you stop. If you fully pull, you stop. If you just pull a little bit, you can move. This is not linear.

Drivers who pull to start moving can immediately assume pulling further would increase the speed, rather than decrease.

This less intuitive control scheme... is acceptable due to the engineering design of the handlebar being more important (its pretty safe if the easiest thing to do is stop).

<a name="closing"></a>

&nbsp;
<h2><strong>closing: on constraints and go-karts</strong></h2>
Whew. Actual safety constraints sure are something huh? They make the road planning straightforward, and you're limited on the gimmicks you can introduce (they all have to be crash-safe i.e. they are all soft, weighted foam blocks you can run into).

You can't have Mario Kart items because its real life and you don't want people to crash.

Speaking of which, lets talk about go-karts. Isn't the design going to be very similar? Yes, and also no. The supreme design constraint of "don't overwhelm the player" comes into play here.

Go-karts already demand enough attention from their much nicer acceleration. Nice enough acceleration and top speeds to result in more serious collisions with walls or other go-karts. <strong>There's too much operating risk</strong> in combining go-karts with mountain-pass track features.

Finally, there is an <strong>important question to the designer,</strong> a personal one. Is it okay? <strong>Are you fine with</strong> <strong>the mountain naturally deciding the game flow? </strong>Does that make one feel less in control as a designer? Or as a designer, should this be a blessing that the design is already decided?

Its generally good. The presence of the mountain also the track<em> intuitive</em>. There's no study on whether player frustration from falling off rainbow road is due to how <em>abstract</em> it is.

Anyway, I'll stick to blogging about video games, where the player is safe and our imagination is powerful enough to move mountains instead.

Have fun out there won't you?

<strong>[3. a look at luge design]</strong>

<a href="#whatsaluge">Whats a Luge</a> &gt; <a href="#thedesign">The Design</a> &gt; <a href="#driversnotes">Drivers Notes</a> &gt; <a href="#closing">Closing</a>
