---
layout: blog
title: Android backups, Google fail.
tags: geekery, android, backups
---

I've not managed to update this blog for a few weeks, I've been busy sunning myself in Southern France. It's a hard life.

Returning to form, here's a geeky update.

My phone, a Nexus 4, bricked recently. This may have been down to the Android 4.4.3 system update that I'd done the day before, I'm not really sure, but it was dead. For a while I thought it was completely gone, but after messing about for a while I managed to coax it into recovery mode. For the record you do this my holding down all three buttons until it starts up and then you can select recovery mode from the menu that appears.

From recovery mode, the advice on the support forums was to do a full factory reset. This shouldn't have been a problem, being a geek the first thing I do with any new device is work out how to back it up just in case this sort of thing happens. In the Apple world, back when I had an iPhone, this was done through iTunes; in the Android world it's done by Google and configured in Settings &rarr; Backup & restore.

<img class="img-responsive venter-block" src="/img/Screenshot_2014-07-03-21-15-41.png">
(The backup account is configured, I'm just not splashing my Google account ID all over the internet...)

So that takes care of that, everything's backed up to Google, I can do my hard reset and everything will be fine. Right?

Wrong.

What actually happened was this. My phone booted up as if it was new out of the box and it asked me to log into the WiFi and then to log in with my Google account, so far so good. It then asked me if I wanted to restore from backup. Yes! I thought, this is what I was expecting to happen and told my phone to go ahead.

So what did the backup actually restore? Not much is the answer. It restored all my saved wireless SSIDs and WPA keys (can't think why Google are keen to keep that information [after they were told to delete their previous dataset](http://www.theregister.co.uk/2013/06/21/ico_orders_google_to_destroy_wifi_payload_data_in_next_35_days/) ) and it redownloaded all my installed apps for me from the Play Store, without any of their settings or data.

That was it. It hadn't kept and of the apps' data, it didn't put the apps back where they were on my home screen (it just left them in a big unconfigured heap in the app drawer) none of my text messages were backed up, none of the system settings were where I left them, nothing. 

That's rubbish.

Google, that barely qualifies as a backup, that's just you pulling the information you want off my phone and keeping a list of what apps I've got. Last time I checked a backup was supposed to be about protecting **data**. 

I'm unimpressed to say the least.

As it turns out, I haven't actually lost all that much. Most of my data is kept in the cloud anyway these days, all my pictures are backed up independently using Dropbox Camera Upload (<https://www.dropbox.com/help/289/en>) so it's mostly just a PITA having to log back into everything, putting everything back where it was and resyncing all the cached data. The only things that're lost forever are my text messages, but I can live without those.

Verdict: 1 out of 10, must try harder.

So lazyweb, I can't be the only person to have hit this issue. As the in-built system is clearly a pile of pants, what's the best way of backing up an Android phone?
