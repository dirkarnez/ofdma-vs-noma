# ofdma-vs-noma
NOMA (Non-Orthogonal Multiple Access) and OFDMA (Orthogonal Frequency Division Multiple Access) are both wireless channel access technologies, but they separate and assign users to the spectrum in fundamentally different ways. [1] (https://www.hilarispublisher.com/open-access/performance-evaluation-of-energy-efficiency-and-spectral-efficiency-noma-vs-ofdma.pdf), [2] (https://www.rfwireless-world.com/terminology/noma-vs-ofdma)

Core Differences


Feature	OFDMA (Orthogonal Frequency Division Multiple Access)	NOMA (Non-Orthogonal Multiple Access)
Basic Principle	Splits bandwidth into orthogonal (non-overlapping) time and frequency sub-channels (Resource Units).	Allows multiple users to share the exact same time and frequency resources simultaneously.
Domain Used	Time and Frequency domain.	Power domain (or code/interleave domain).
Multiplexing	One user per specific sub-channel at any given moment.	Multiple users layered on top of each other using different power levels.
Transmitter Action	Assigns distinct slices of frequency/time to each device.	Uses superposition coding to combine user messages at different power allocations.
Receiver Action	Simple filtering/decoding of its assigned sub-channel.	Uses Successive Interference Cancellation (SIC) to decode and subtract stronger/weaker signals.
Spectral Efficiency	Lower to moderate; wastes empty sub-channel space if a user isn't sending heavy data.	Higher; improves system throughput and spectral efficiency (up to 1.78x–2.538x in studies).
Receiver Complexity	Low.	High (due to SIC processing and error propagation risks).


How OFDMA Works

• Mechanism: OFDMA divides a wide channel (like 20 MHz or 40 MHz in Wi-Fi 6/7 or cellular LTE/5G) into smaller sub-carriers grouped into Resource Units (RUs). [1] (https://www.youtube.com/watch?v=T-b3__nEskw), [2] (https://www.youtube.com/watch?v=iuSybfOyiU8)
• User Isolation: Each user gets a dedicated slice of frequency and time. User A does not interfere with User B because their signals are strictly orthogonal. [1] (https://www.hilarispublisher.com/open-access/performance-evaluation-of-energy-efficiency-and-spectral-efficiency-noma-vs-ofdma.pdf), [2] (https://www.rfwireless-world.com/terminology/noma-vs-ofdma), [3] (https://www.youtube.com/watch?v=T-b3__nEskw)
• Where it’s used: Extensively used in 4G LTE, 5G NR (downlink/uplink), and modern Wi-Fi (Wi-Fi 6 / 802.11ax and Wi-Fi 7) via tools like the Cisco OFDMA Guide. [1] (https://www.cisco.com/site/us/en/learn/topics/networking/what-is-ofdma.html), [2] (https://www.netspotapp.com/blog/wifi-standards/what-is-ofdma.html), [3] (https://www.rfwireless-world.com/terminology/noma-vs-ofdma), [4] (https://www.youtube.com/watch?v=T-b3__nEskw)

How NOMA Works

• Mechanism: Instead of splitting the frequency grid into strict boxes, NOMA lets multiple users transmit over the same frequency and time at once. [1] (https://www.hilarispublisher.com/open-access/performance-evaluation-of-energy-efficiency-and-spectral-efficiency-noma-vs-ofdma.pdf), [2] (https://www.techplayon.com/explaining-noma-basic-concept-different-ofdma-applications-noma-5g/)
• User Isolation: Users are separated by power levels based on their channel conditions (e.g., a cell-edge user with a weak signal gets more power, while a cell-center user with a strong signal gets less power). [1] (https://www.techplayon.com/explaining-noma-basic-concept-different-ofdma-applications-noma-5g/)
• Decoding (SIC): The receiver at the stronger user first decodes the higher-power signal (intended for the other user or itself), subtracts it out using Successive Interference Cancellation (SIC), and then decodes its own data. [1] (https://www.linkedin.com/pulse/noma-vs-ofdma-whats-next-wi-fi-manoj-kumar-kancharana-opxoc)
• Where it’s used: Explored heavily for advanced 5G/6G deployment scenarios to maximize spectral and energy efficiency, as analyzed in technical breakdowns on RF Wireless World. [1] (https://www.hilarispublisher.com/open-access/performance-evaluation-of-energy-efficiency-and-spectral-efficiency-noma-vs-ofdma.pdf), [2] (https://www.rfwireless-world.com/terminology/noma-vs-ofdma)

Pros and Cons Summary

• OFDMA Advantages:
	• Low receiver complexity.
	• Reliable, predictable, and widely standardized.
	• Less sensitive to channel estimation errors. [1] (https://www.hilarispublisher.com/open-access/performance-evaluation-of-energy-efficiency-and-spectral-efficiency-noma-vs-ofdma.pdf)
• OFDMA Disadvantages:
	• Hard limits on how many users can fit into the time-frequency grid.
	• Sub-optimal spectral efficiency when traffic is bursty or small. [1] (https://blog.csdn.net/qq_35027690/article/details/162845050), [2] (https://www.youtube.com/watch?v=T-b3__nEskw)
• NOMA Advantages:
	• Superior spectral efficiency, higher sum-rates, and massive user density.
	• Greatly benefits edge-of-cell or power-limited devices by letting them share bandwidth. [1] (https://zenodo.org/records/20280987), [2] (https://www.hilarispublisher.com/open-access/performance-evaluation-of-energy-efficiency-and-spectral-efficiency-noma-vs-ofdma.pdf), [3] (https://blog.csdn.net/qq_35027690/article/details/162845050), [4] (https://www.techplayon.com/explaining-noma-basic-concept-different-ofdma-applications-noma-5g/)
• NOMA Disadvantages:
	• High computational and hardware complexity at the receiver (SIC).
	• Vulnerable to error propagation if SIC fails or Channel State Information (CSI) is imperfect.
	• Fair-sharing challenges for users with poor signal-to-noise ratios (SNR). [1] (https://assets-eu.researchsquare.com/files/rs-5458986/v1_covered_7c5f8bd4-46ec-4d24-9eeb-9ef1bf2b9547.pdf), [2] (https://www.hilarispublisher.com/open-access/performance-evaluation-of-energy-efficiency-and-spectral-efficiency-noma-vs-ofdma.pdf), [3] (https://zenodo.org/records/20280987)
Would you like to explore how Successive Interference Cancellation (SIC) works in detail, or look at how NOMA and OFDMA are applied in 5G and Wi-Fi standards?
