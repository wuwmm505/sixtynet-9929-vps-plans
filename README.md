# 9929 VPS: SixtyNet plans from $200/year, why residential IPs block ports 80 and 443, and when a $26/year box is the better buy

SixtyNet's cheapest AS9929 plan costs **US$200 a year**: 2 cores, 2 GB RAM, 40 GB NVMe, 5 TB of monthly traffic on a 2 Gbps port, with DDoS protection included. The cheapest Los Angeles 9929 boxes sold elsewhere start near **US$26 a year**. Both numbers are accurate, and the gap between them is the whole decision.

Buy SixtyNet when you actually move multiple terabytes a month at gigabit-plus port speeds. If you are still trying to find out whether 9929 feels better than your current line, a $26–43/year plan answers that question for roughly a seventh of the price. Per gigabyte of traffic, SixtyNet is the cheaper of the two; per month of ownership, it is the most expensive option on this page.

> **Quick picks**
>
> - **5 TB+/month, gigabit ports, DDoS cover:** LAX-STARTER at $200/year. Step up to LAX-MICRO at $400/year when you need 4 cores and 10 TB.
> - **Residential IP for streaming, AI tools or account work, no public site:** Residential-STARTER at $25/month. Ports 80 and 443 stay closed on this line.
> - **Cheapest way to test 9929:** not SixtyNet. Comparable LA plans run US$26–43/year.
>
> 👉 [See SixtyNet's current 9929 plan list and prices](https://sixtynet.net/aff.php?aff=39)

## SixtyNet's 9929 lineup, plan by plan

SixtyNet splits its Los Angeles 9929 stock into two billing models. The LAX-* plans are sold annually with DDoS protection and standard traffic allowances. The residential-IP plans run on monthly billing, come with 10 Gbps ports, and carry restrictions that decide whether the plan is usable for you at all.

### LAX line (annual billing, DDoS protection included)

| Plan | vCPU / RAM | NVMe / traffic | Port | Price | Order |
| --- | --- | --- | --- | --- | --- |
| LAX-STARTER | 2 / 2 GB | 40 GB / 5 TB | 2 Gbps | $200/yr (list $240) | [Order](https://sixtynet.net/aff.php?aff=39) |
| LAX-MICRO | 4 / 4 GB | 80 GB / 10 TB | 4 Gbps | $400/yr (list $480) | [Order](https://sixtynet.net/aff.php?aff=39) |
| LAX-MEDIUM | 8 / 8 GB | 160 GB / 20 TB | 10 Gbps | $800/yr (list $960) | [Order](https://sixtynet.net/aff.php?aff=39) |
| LAX-LARGE | 8 / 16 GB | 320 GB / 40 TB | 10 Gbps | $1,600/yr (list $1,920) | [Order](https://sixtynet.net/aff.php?aff=39) |
| China Unicom-Premium (BGP group) | 2–16 / 2–16 GB | 40–320 GB / 5–40 TB | 100 Mbps base, 3× burst | $2,500/yr (list $3,000) | [Order](https://sixtynet.net/aff.php?aff=39) |

The last row is a different product class. That group advertises free BGP session setup, limited BGP technical support, 95th-percentile billing and a 100 Mbps base commit with 3× burst, which is language aimed at network operators and multi-homed setups rather than someone renting a single VPS. If you do not know what 95th-percentile billing means for your bill, this tier is not for you.

### Residential and storage line (monthly billing)

| Plan | vCPU / RAM | NVMe / traffic | Price | Order |
| --- | --- | --- | --- | --- |
| Residential-STARTER | 2 / 2 GB | 40 GB / 5 TB | $25/mo | [Order](https://sixtynet.net/aff.php?aff=39) |
| Residential-MICRO | 4 / 4 GB | 80 GB / 10 TB | $45/mo | [Order](https://sixtynet.net/aff.php?aff=39) |
| Residential-MEDIUM | 8 / 8 GB | 160 GB / 20 TB | $85/mo | [Order](https://sixtynet.net/aff.php?aff=39) |
| Residential-LARGE | 8 / 16 GB | 320 GB / 40 TB | $165/mo | [Order](https://sixtynet.net/aff.php?aff=39) |
| IRVINE-PRO-STARTER | 2 / 2 GB | 40 GB / 5 TB | $35/mo | [Order](https://sixtynet.net/aff.php?aff=39) |
| IRVINE-PRO-MICRO | 4 / 4 GB | 80 GB / 10 TB | $55/mo | [Order](https://sixtynet.net/aff.php?aff=39) |
| LAX-Storage-500G | 4 / 4 GB | 300 GB + 200 GB bonus, RAID 10 / 10 TB | $40/mo | [Order](https://sixtynet.net/aff.php?aff=39) |
| LAX-Storage-1TB | 8 / 8 GB | 1000 GB / 15 TB | $70/mo | [Order](https://sixtynet.net/aff.php?aff=39) |

Traffic figures are monthly. The annual LAX prices come from SixtyNet's own VPS Hosting page, which presents them as 17% below list. The monthly residential and storage rates are the figures published by third-party plan trackers in September 2026 for the same core/RAM/storage/traffic combinations; confirm them on the order page before paying.

Three restrictions on this list matter more than any spec:

- **Residential plans block ports 80 and 443.** SixtyNet states this is for IP risk-control reasons. You cannot host a public website on Residential-STARTER through LARGE. Period.
- **The IRVINE-PRO variants are whitelist-only.** The product description says the machine rejects external probes and scans, and is unreachable unless you configure trusted IPs or port forwarding. That is excellent for privacy and useless for anything that needs to accept inbound connections from the public internet.
- **Refunds on those PRO variants go to your SixtyNet balance**, not back to your card. The product page says so directly.

Port policy on the LAX-* plans is not stated the same way, so if you plan to migrate a live site, ask support to confirm 80/443 are open on the specific plan before you pay for a year.

## What AS9929 actually buys you

AS9929 is China Unicom's premium backbone, known in the Chinese hosting market as 联通 9929. Its selling point is the return path: traffic back to mainland China rides Unicom's premium link, with telecom users returning via 9929 to 163, Unicom users connecting directly, and mobile users going 9929 to CMI. In practice that means less packet loss and flatter latency at peak evening hours, which is why it gets used for sites with mainland visitors, remote work and relay nodes.

Positioned against the two obvious alternatives, the industry view is consistent: 9929 is generally regarded as a step above AS4837 in quality and a step above it in price, while CN2 GIA is more expensive again and stronger specifically on the telecom return path. None of this is official Unicom documentation. It is the consensus among the sellers and reviewers who work with these lines daily, and it holds up well enough to plan a purchase around.

What 9929 does not fix is your own access network. If your ISP's international routing is the bottleneck, a premium return path will not compensate. That is the argument for testing cheaply first, covered below.

## The cost comparison that decides this

Entry-level 9929 capacity in Los Angeles is now genuinely cheap. Here is what the same category of product costs at four other sellers, all figures as published by third-party plan tables and catalogs:

| Seller | Entry 9929 plan | Monthly equivalent | Traffic |
| --- | --- | --- | --- |
| SixtyNet | LAX-STARTER, 2C/2G, $200/yr | $16.67 | 5 TB |
| QQG | 1C/1G, $25.99/yr | $2.17 | 200 GB (per plan name) |
| Back Waves | 1C/1G, HK$26.90/mo | ~$3.43 | not listed |
| VMISS | 1C/1G/10 GB, C$5.00/mo | ~$3.60 | 500 GB |
| LisaHost | 1C/1G/10 GB, 199 CNY/yr | ~$2.30 | 200 GB |

Flip the math to cost per terabyte of monthly traffic and the ranking reverses. SixtyNet's LAX-STARTER works out to about **$3.33 per TB-month**. The QQG entry plan is roughly $10.85 per TB-month at its 200 GB allowance; VMISS lands near $7.20; LisaHost near $11.50. SixtyNet is two to three times cheaper per unit of traffic while being seven to eight times more expensive per calendar month.

Both readings are correct, and which one applies depends on a single question: will you actually use five terabytes? A blog, a personal proxy or a small API will not come close, and paying $200 a year for idle capacity is a bad trade no matter how good the per-TB rate looks. A scraper, a media pipeline, a backup target or a relay serving several people will blow through 200 GB in a week, and the cheap annual plans become the expensive option once overage or throttling kicks in.

QQG's numbers come from a plan table its own compiler flagged as unconfirmed with the provider, and one row in that table lists a 4C/4G plan name against a 2 vCPU/2 GB configuration. Treat those figures as a price band, not a quote.

## Who should not buy SixtyNet

**Anyone testing 9929 for the first time.** Spend $26–43 on an annual plan from a budget seller, run it through two weeks of evening peak traffic, and only then decide whether the line is worth a $200 commitment. SixtyNet's annual terms and lack of a published refund window on the LAX line make it a poor instrument for experiments.

**Anyone who needs a website on a residential IP plan.** Ports 80 and 443 are closed by design. The residential line is for outbound work: streaming unlocks, AI service access, account management, scrapers.

**Anyone who needs a public-facing machine with no inbound filtering.** The IRVINE-PRO plans are deliberately unreachable without a whitelist. That is the feature, and it is also the constraint.

**Anyone who wants a documented money-back guarantee.** SixtyNet's product pages spell out a refund route only for the whitelist-only residential variants, and that route credits your account balance. Other 9929 sellers publish a 48-hour unconditional refund window. If the ability to walk away matters to you, get the refund terms in writing from support before paying for twelve months upfront.

👉 [Check SixtyNet's plan page before committing to an annual term](https://sixtynet.net/aff.php?aff=39)

## Before you pay: five things to confirm

1. **Billing cycle and renewal price.** The LAX line is advertised annually at 17% below list. Ask what the renewal rate is and whether the discount recurs, because a $200 first year that renews at $240 changes the math slightly, and a bigger step would change it a lot.
2. **Port policy on your specific plan.** Confirmed in writing for anything you intend to serve traffic from.
3. **Traffic overage handling.** Whether exceeding 5 TB throttles the port, bills overage, or suspends service is not spelled out on the plan list. Ask.
4. **IPv6.** A July 2026 third-party review of the residential line reported no IPv6 support. If you need it, verify with support.
5. **Payment methods and refund route.** Both affect how quickly you can exit if the line underperforms on your network.

## FAQ

**Is 9929 better than 4837?**
Generally yes on peak-hour stability, and you pay for it. 4837 tends to offer more bandwidth per dollar with slightly looser latency at peak. Pick 4837 for bulk transfer where a few extra milliseconds do not matter, 9929 where interactive latency does.

**Can I host a website on SixtyNet's 9929 plans?**
On the LAX-* line, probably, but confirm 80/443 with support first. On the residential line, no. Those ports are closed to reduce IP risk-control flags.

**What is the difference between a residential IP and a native IP?**
A native IP is registered in the target country. A residential IP additionally sits on a consumer ISP's last-mile network, so services that check connection type see home broadband rather than a data center. SixtyNet's residential plans run over Cox Communications infrastructure in Orange County, California, according to third-party reviews. That is what makes them useful for platforms that penalize data center ranges, and what makes them expensive.

**Can I install Windows?**
Third-party plan listings note Windows installation for the residential and storage lines. Confirm on the order page for the LAX plans if that is a requirement.

**What happens if the IP gets blocked?**
Residential IPs are less likely to be flagged, which is the point of paying for them. There is no published policy on replacement IPs for the standard line, so ask support how they handle it before you depend on one IP for anything long-lived.

## Picking a plan

Run the numbers against your actual monthly egress before anything else. Under 500 GB, buy a $26–43/year plan elsewhere and keep your money. Between 1 and 4 TB, the Residential-STARTER at $25/month is the interesting option if your workload is outbound and you can live without ports 80 and 443; if you need a public site, the LAX-STARTER at $200/year is the entry point and its 5 TB will not be the limiting factor. Above 10 TB with multi-gigabit bursts, LAX-MICRO or LAX-MEDIUM is where the per-TB math starts working in your favor.

Skip the China Unicom-Premium BGP tier and the IRVINE-PRO whitelist plans unless you specifically need BGP peering or a machine that cannot be scanned.

👉 [Compare SixtyNet's 9929 plans and choose a billing cycle](https://sixtynet.net/aff.php?aff=39)
