Hey everyone, I wanted to share a custom TradingView indicator I put together called the Bookmap Style Heatmap + Volume Bubbles. It’s designed to bring order-flow style visualization right onto your main chart so you don't have to constantly look away to a separate volume panel.

Here is a quick breakdown of what it does and how to read it:

The Background Heatmap
Instead of a traditional volume profile anchored to the side of your screen, this script paints a thermal map directly over your recent price action. It takes a lookback period (which defaults to 80 bars) and slices the high-to-low range into a grid of horizontal price levels. It then distributes the volume across the specific levels where the trading actually happened.


To keep your TradingView charts running smoothly and avoid hitting drawing limits, the script actively deletes old heatmap boxes and only renders the profile on the most recent bar.


The colors act as a density gradient so you can spot liquidity at a glance: it starts at dark blue and aqua for low volume zones, moves up into lime and yellow for moderate volume, and flashes red for your peak volume concentration levels.

Dynamic Volume Bubbles
This feature helps you instantly spot capitulation, breakouts, or aggressive market participation. The script tracks a moving average of the volume (defaulting to a 100-period length). If a new candle's volume spikes past your set multiplier—like 1.5x the average—it plots a bubble right at the midpoint of that candle.


If the candle closed higher than it opened, you get a lime "Buy" bubble, and if it closed lower, you get a red "Sell" bubble.


The best part is that the bubbles dynamically scale in size based on the intensity of the spike. A standard spike gets a normal-sized bubble, but if the volume pushes past 2.5x or even 4x the average, the bubbles become progressively larger (scaling from large to huge) so you absolutely cannot miss the big players stepping in.


Customization
Everything is fully adjustable in the indicator settings. You can tweak the lookback periods, change the amount of price level rows for more or less heatmap granularity, and adjust the exact volume multipliers required to trigger the bubbles. You can also completely toggle the heatmap or the bubbles on and off if you prefer a cleaner chart.

Just copy the source code, paste it into your Pine Editor, and add it to your chart!
