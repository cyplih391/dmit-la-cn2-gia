# Best Los Angeles VPS: Is a $72.90/Month CN2 GIA Plan Overkill, What Do AS9929 and CMIN2 Actually Change, and How Do DMIT's Refunds Work? (Full Plan Table)

Los Angeles VPS pricing currently runs from about $2.48 a month for a 512 MB sandbox to just over $1,000 a month for a 12-core machine with 50 TB of transfer. Most of that spread comes from two things: how many dedicated cores you get, and which route your traffic takes on the way back to China. DMIT sits at the premium end on both. Its LAX Pro line runs on AMD EPYC 9004 and 9005 hardware, ships 10 Gbps ports, and sends all three Chinese carriers home over CN2 GIA (AS4809). Entry is **$72.90/month** on the AN4 platform and **$79.90/month** on AN5.

Below is the full LAX Pro table, an explanation of what each route acronym buys you, the buyers who should not pay for GIA at all, and the refund clauses that determine whether you can walk away from a plan that does not fit.

> **Quick pick:** if your visitors or your own connection are in mainland China and you want the return path handled for Telecom, Unicom and Mobile in one plan, the **LAX.AN4.Pro.MINI at $72.90/month** (4 vCPU, 4 GB, 80 GB SSD, 10 Gbps port, 5 TB) is the cheapest way into DMIT's Los Angeles Pro tier. If your audience is mostly outside China, this tier costs more than the problem it solves. 👉 [Check DMIT's current Los Angeles Pro stock](https://www.dmit.io/aff.php?aff=9081)

## DMIT's Los Angeles Pro lineup, every tier listed

DMIT splits its Los Angeles catalog by hardware platform: AS3 on EPYC 7003, AN4 on EPYC 9004, AN5 on EPYC 9005. The Pro series is the CN2 GIA one, where return traffic from all three Chinese carriers rides AS4809. These are the Pro tiers published for the two newest platforms.

| Plan | vCPU · RAM · SSD | Port · Monthly transfer | Price | Order |
| --- | --- | --- | --- | --- |
| LAX.AN4.Pro.MINI | 4 · 4 GB · 80 GB | 10 Gbps · 5 TB (8 Mbps after) | $72.90/mo | [Order LAX.AN4.Pro.MINI](https://www.dmit.io/aff.php?aff=9081) |
| LAX.AN4.Pro.MICRO | 4 · 4 GB · 160 GB | 10 Gbps · 7 TB (8 Mbps after) | $102.90/mo | [Order LAX.AN4.Pro.MICRO](https://www.dmit.io/aff.php?aff=9081) |
| LAX.AN4.Pro.MEDIUM | 6 · 8 GB · 160 GB | 10 Gbps · 14 TB (10 Mbps after) | $239.90/mo | [Order LAX.AN4.Pro.MEDIUM](https://www.dmit.io/aff.php?aff=9081) |
| LAX.AN4.Pro.LARGE | 8 · 16 GB · 320 GB | 10 Gbps · 25 TB (10 Mbps after) | $459.90/mo | [Order LAX.AN4.Pro.LARGE](https://www.dmit.io/aff.php?aff=9081) |
| LAX.AN4.Pro.GIANT | 12 · 24 GB · 640 GB | 10 Gbps · 50 TB (10 Mbps after) | $929.90/mo | [Order LAX.AN4.Pro.GIANT](https://www.dmit.io/aff.php?aff=9081) |
| LAX.AN5.Pro.MINI | 4 · 4 GB · 80 GB | 10 Gbps · 5 TB (8 Mbps after) | $79.90/mo | [Order LAX.AN5.Pro.MINI](https://www.dmit.io/aff.php?aff=9081) |
| LAX.AN5.Pro.MICRO | 4 · 4 GB · 160 GB | 10 Gbps · 7 TB (8 Mbps after) | $110.90/mo | [Order LAX.AN5.Pro.MICRO](https://www.dmit.io/aff.php?aff=9081) |
| LAX.AN5.Pro.MEDIUM | 6 · 8 GB · 160 GB | 10 Gbps · 14 TB (10 Mbps after) | $289.90/mo | [Order LAX.AN5.Pro.MEDIUM](https://www.dmit.io/aff.php?aff=9081) |
| LAX.AN5.Pro.LARGE | 8 · 16 GB · 320 GB | 10 Gbps · 25 TB (10 Mbps after) | $499.90/mo | [Order LAX.AN5.Pro.LARGE](https://www.dmit.io/aff.php?aff=9081) |
| LAX.AN5.Pro.GIANT | 12 · 24 GB · 640 GB | 10 Gbps · 50 TB (10 Mbps after) | $1,009.90/mo | [Order LAX.AN5.Pro.GIANT](https://www.dmit.io/aff.php?aff=9081) |

The figure in brackets is what your port drops to once the monthly transfer allowance is used up. Traffic keeps flowing, unmetered, at 8 or 10 Mbps. You will not get a surprise overage invoice, and you will not get full speed either.

Stock is the other thing to plan around. The most recent restock covered only the Pro.MINI and Pro.MICRO tiers on both AN4 and AN5. The older AS3 platform on EPYC 7003 replenishes roughly once a month, sometimes longer, and it is where the lower entry prices have historically sat. If the tier you want shows as unavailable, waiting a few weeks is the realistic option rather than picking a different size. 👉 [See what is in stock on the LAX Pro line](https://www.dmit.io/aff.php?aff=9081)

## What CN2 GIA, AS9929, CMIN2 and AS4837 actually change

Every Los Angeles VPS crosses the Pacific on fibre you do not control. What you are buying with a premium plan is the queue your packets sit in once they reach a Chinese network.

- **AS4134 (163 backbone)** is China Telecom's default international path. It is cheap, widely available, and visibly congested between roughly 8pm and midnight Beijing time.
- **AS4809, CN2 GIA** is Telecom's premium network. Capacity is limited and carriers charge for it, which is why plans that use it cost what they do. GIA is the tier that keeps working at peak.
- **AS4837** is China Unicom's international line, the backbone most "CU-optimized" plans lean on.
- **AS9929** is Unicom's premium network, often labelled CUII. It is the Unicom equivalent of what GIA does for Telecom.
- **AS58453 (CMI)** and **AS58807 (CMIN2)** are China Mobile International's regular and second-generation premium routes.

A plan described as "three-network optimized" is making a claim about the return path for all three carriers. Many plans only optimize one or two and leave the third on commodity transit, which shows up as one carrier performing badly while the other two look fine in a speed test run by someone on a different ISP than you.

DMIT's LAX Pro routing, as published: outbound from the VM, Telecom goes over GIA (AS4809), Unicom goes direct over AS4837, Mobile goes out through Hong Kong Mobile (AS58453). Return traffic from all three carriers comes back over GIA (AS4809). That asymmetry is worth understanding. Outbound performance from your server to a Chinese visitor is not identical to inbound performance from that visitor, and the return leg is the one that usually decides whether a page feels fast.

## Who should not buy the Pro tier

This is the part most Los Angeles VPS write-ups skip, because the answer costs them a sale.

**Your audience is outside China.** If your users are in California, Oregon, Washington, or anywhere in Europe, the return route to Chinese carriers is irrelevant to them. You would be paying a routing premium that does nothing for your traffic. A $2.48 to $15/month international-transit VPS covers that job.

**You need a US exit node for US services.** A VPN or proxy endpoint used from China benefits from GIA. One used to reach US-only services from elsewhere does not, and the entry price here is high for a single-purpose box.

**You are buying compute, not latency.** At $72.90/month the smallest Pro plan gives you 4 vCPU and 4 GB. If your workload is compilation, transcoding, or game servers, that money is better spent on dedicated cores; the section further down covers that comparison.

**You run a small personal site.** 4 vCPU and 5 TB of transfer is enterprise-shaped. At $72.90 monthly, a year of the MINI tier costs $874.80, and there is no smaller Pro option to step down to.

## Year one, year two, and the throttling clause

The published LAX Pro prices are monthly rates, not discounted first-term teasers, so year two costs what year one costs: $874.80 for the AN4 MINI, $958.80 for the AN5 MINI. Budget on that basis rather than on a promo figure that will reset.

Overages are handled by throttling instead of billing. The 8 Mbps ceiling on MINI and MICRO sustains a website, an API, or an SSH session perfectly well. It does not sustain video, large file sync, or a busy download endpoint. If your monthly transfer sits anywhere near 5 TB, size up to a 10 Mbps tier rather than discovering the limit at 11pm on a Friday.

The 10 Gbps port figure is a port speed. Single-connection throughput to any one destination will be decided by the return route and your own last mile, not by that number.

## The refund rules decide more than the price does

DMIT publishes a full refund within **3 days** of purchase, provided you have used no more than **30 GB** of transfer. Within **30 days** you can get a partial refund of the remaining value, calculated against remaining transfer or remaining service time, whichever is lower, minus the payment gateway's fee.

What matters more is the excluded list. Refunds are **not** granted when the network is not good enough for you, when the problem is IP geolocation, when the instance is targeted by DDoS, after three refunds on the same product series, for abuse-related losses, or if you open a chargeback dispute with your payment provider. The same document notes that if an IP is unreachable in some region but you have already pushed past 3 GB of traffic, the refund path closes.

Read that combination carefully, because it shapes how you should buy. You get 72 hours and 30 GB to decide whether the routing works from your location. That is enough for traceroutes, ping tests from several Chinese provinces, and a day of real use. It is not enough to wait a week for a peak-hour slowdown to reveal itself. Run the tests on day one.

Refunds to DMIT credit carry no fee. Refunds to the original payment method lose the gateway's handling charge, with Alipay called out as the exception where the fee is returned. Requests are typically processed within 48 hours, and the instance is stopped when you file, so back up anything you need before you start the process. Data is unrecoverable once the refund completes.

## Hardware per dollar: two non-GIA reference points

If routing is not your constraint, the comparison shifts entirely to cores and storage.

| Provider | Reference tier | Price | Notable detail |
| --- | --- | --- | --- |
| Cloudzy | 512 MB · 20 GB NVMe · 1 TB at 40 Gbps | $2.48/mo (listed 50% off $4.95) | 14-day money-back, 99.95% SLA, hourly or monthly billing, EPYC, dedicated IPv4 + IPv6 |
| Cloudzy | 4 GB · 120 GB NVMe · 5 TB at 40 Gbps | $14.48/mo | 2 vCPU, same refund and SLA terms |
| Bloom.Host | 8 GB · 120 GB NVMe · 4 TB | $30/mo | Dedicated KVM cores, no CPU fair-use policy, Ryzen 9 up to 9950X, DDoS filtering advertised at 400+ Tbps |

Cloudzy's Los Angeles region runs on AMD EPYC with NVMe throughout and provisions in about 60 seconds; its 14-day money-back window is more than four times DMIT's. Bloom.Host's tier comparison carries a data stamp of May 8, 2026, and its pitch is the opposite of DMIT's: dedicated cores and zero overselling rather than optimized China routing.

Neither is a substitute for a GIA plan if GIA is what you need. They are what you buy when it is not.

## Before you order

1. Confirm the exact tier is in stock. Restocks are batchy and the MINI tiers disappear first.
2. Run your latency tests inside the 3-day window, from the provinces your users are actually in.
3. Stay under 30 GB of transfer until you have decided to keep the machine.
4. Check whether your intended use falls under an excluded refund reason. IP geolocation is the one that catches streaming buyers.
5. Confirm the payment method's refund handling before you pay, since gateway fees come out of the partial refund.

## Questions that come up

**Can I get a refund if the route is slow for me?** No. "The network is not good enough" is listed as a non-refundable reason. Test inside the 3-day full-refund window instead.

**Will the LAX Pro IP unlock Netflix or similar?** DMIT's plan documentation covers hardware and routing, not streaming catalogs, so there is no published claim to rely on. IP geolocation is also an excluded refund reason, which makes this a poor basis for a $72.90 purchase.

**Is there a cheaper DMIT Los Angeles plan?** The AS3 platform on EPYC 7003 sits below AN4 and AN5 and restocks about monthly. It is the tier to watch if the Pro entry price is above your budget.

**Do I need the 10 Gbps port?** For almost nobody. The return route and your own connection set the ceiling.

**Can I pay with Alipay?** It appears in DMIT's refund documentation as a supported method, and it is the one where the gateway fee is returned rather than deducted.

## Which tier fits which buyer

Serving mainland users across all three carriers, with a budget that tolerates $874.80 a year: take the **LAX.AN4.Pro.MINI at $72.90/month**. It is the cheapest route into three-network GIA on current EPYC hardware.

Want the newest EPYC generation and $7 a month is not the deciding factor: the **AN5 MINI at $79.90/month** is the same shape on newer silicon.

Need more than 5 TB, more than 4 cores, or a 10 Mbps throttle floor instead of 8: step to MICRO, MEDIUM, or above.

Audience outside China, or a single-purpose US exit node: skip this tier and spend $2.48 to $15 elsewhere.

Compute-heavy workload that needs dedicated cores: Bloom.Host's 8 GB tier at $30/month is the better use of the money.

One last check before you pay: confirm the tier is actually in stock and that your planned use does not land on the non-refundable list. 👉 [Start with DMIT's Los Angeles Pro plans](https://www.dmit.io/aff.php?aff=9081)
