# RackNerd VPS plans: which one runs Ollama, n8n or OpenClaw, do renewals go up, and what does $21.99 a year actually get you? (full plan table)

RackNerd's cheapest VPS is **$21.99 a year** for 1 GB of RAM. The plan most self-hosters end up needing costs **$59.99 a year**, and the reason is written into RackNerd's own FAQ: Ollama, LibreChat, AnythingLLM and Hermes Agent each want at least 4 GB of RAM, while OpenClaw wants at least 8 GB, which puts you on the **$119.99/year** tier. The same FAQ settles the renewal question. These specials are "lifetime recurring," so the annual rate you sign up at is the rate you keep paying.

What follows is the five plans exactly as listed on RackNerd's VPS Specials page, the per-app RAM floors from that page, the arithmetic behind each upgrade step, and the parts of the offer that decide whether it fits you at all: one IPv4 per server, no refunds, and an unmanaged box you administer yourself.

> Quick pick: **4 GB at $59.99/year** is the smallest plan that clears the 4 GB floor for Ollama, LibreChat, AnythingLLM and Hermes Agent. Running n8n, Coolify or a handful of Docker containers? **2 GB at $35.99/year** is the sensible starting point. 👉 [See all five RackNerd VPS specials, from $21.99/year](https://bit.ly/RacKnerd)

## RackNerd VPS plans and prices

| Plan | vCPU / RAM | SSD | Transfer / month | Price (annual, USD) | Order |
| --- | --- | --- | --- | --- | --- |
| 1 GB KVM VPS | 1 vCPU / 1 GB | 20 GB | 3 TB | **$21.99/yr** | [ 1 GB at $21.99/year](https://bit.ly/RacKnerd) |
| 2 GB KVM VPS | 2 vCPU / 2 GB | 35 GB | 5 TB | **$35.99/yr** | [ 2 GB at $35.99/year](https://bit.ly/RacKnerd) |
| 4 GB KVM VPS | 3 vCPU / 4 GB | 60 GB | 7 TB | **$59.99/yr** | [ 4 GB at $59.99/year](https://bit.ly/RacKnerd) |
| 6 GB KVM VPS | 6 vCPU / 6 GB | 100 GB | 12 TB | **$89.99/yr** | [ 6 GB at $89.99/year](https://bit.ly/RacKnerd) |
| 8 GB KVM VPS | 7 vCPU / 8 GB | 150 GB | 20 TB | **$119.99/yr** | [ 8 GB at $119.99/year](https://bit.ly/RacKnerd) |

Every tier on that page is billed annually and ships with full root access, a 1Gbps network port, one IPv4 address, KVM virtualization, the ctrl control panel and a choice of deployment locations. RackNerd marks the 2 GB plan as "Most popular." Payment provisions the server immediately, so the box is online within minutes rather than after a manual review.

## What does $21.99 a year actually get you?

One vCPU, 20 GB of SSD, 1 GB of RAM and 3 TB of monthly transfer on a 1Gbps port. That is a real server with root SSH, not a container slice, and it handles a static site, a reverse proxy, a monitoring agent, or one small Docker container without complaint.

It is also below the RAM floor of every AI app in RackNerd's one-click catalog. n8n and Coolify start at 2 GB. Ollama, LibreChat, AnythingLLM and Hermes Agent start at 4 GB. So the honest reading of the $21.99 tier is that it exists for the non-AI jobs: a blog, a small API, a jump box, a Docker host running one or two light services. Buy it because your workload is small, not because it is cheap.

The operating system list is CentOS, Rocky Linux, AlmaLinux, Fedora, Debian and Ubuntu. A custom ISO needs a support ticket first; after that you can reinstall from ctrl or mount your own media through the HTML5 console.

## Which plan runs n8n, Ollama, LibreChat or OpenClaw?

RackNerd publishes memory requirements for the apps it installs in one click, and they map cleanly onto the plan ladder:

| App (one-click in ctrl) | RAM floor stated by RackNerd | Cheapest plan that clears it |
| --- | --- | --- |
| n8n, Coolify | 2 GB | 2 GB, $35.99/yr |
| Ollama, LibreChat, AnythingLLM, Hermes Agent | 4 GB | 4 GB, $59.99/yr |
| OpenClaw | 8 GB | 8 GB, $119.99/yr |

Those are vendor-stated minimums, not benchmark results, so treat them as the point where the app is expected to run rather than the point where it runs fast. A 4 GB box with Ollama and LibreChat on it will hold one small model comfortably; loading a second model or a larger quantized one is where the 6 GB or 8 GB tier starts earning its price.

Anything absent from the catalog is still fair game. The one-click installer is a convenience layer over an unmanaged KVM VPS with full root SSH, so Docker, Compose, a custom Python service or a stack nobody has packaged yet installs the same way it would on any other Linux box. When a one-click install finishes, the credentials appear inside the panel, which saves the usual hunt through config files.

👉 [Start on the 4 GB plan at $59.99/year if Ollama or LibreChat is the point](https://bit.ly/RacKnerd)

## The upgrade math: $14, $24, $30, $30

Each step up the ladder costs more than the last in absolute terms, but the amount of hardware you get per dollar changes sharply between the cheap end and the top.

- 1 GB to 2 GB: **+$14/year** for one more vCPU, 15 GB more SSD and 2 TB more transfer.
- 2 GB to 4 GB: **+$24/year** for one more vCPU, 25 GB more SSD and 2 TB more transfer.
- 4 GB to 6 GB: **+$30/year** for three more vCPU, 40 GB more SSD and 5 TB more transfer.
- 6 GB to 8 GB: **+$30/year** for one more vCPU, **50 GB more SSD and 8 TB more transfer**.

The last step is the one worth staring at. For the same $30 that takes you from 4 GB to 6 GB, the 6 GB to 8 GB jump adds half a terabyte of extra SSD and eight more terabytes of monthly bandwidth. If storage or transfer is anywhere near your bottleneck, the 8 GB plan is the better $30.

Divided by RAM, the pricing flattens out fast. The 1 GB plan works out to about $21.99 per GB of RAM per year, the 2 GB plan to roughly $18, and from 4 GB upward every tier lands at approximately **$15 per GB of RAM per year**. RackNerd is not penalizing you for buying more memory at the top of the range. On storage per dollar, the five plans deliver roughly 0.91, 0.97, 1.00, 1.11 and 1.25 GB of SSD per dollar spent; on monthly transfer per dollar, roughly 0.136, 0.139, 0.117, 0.133 and 0.167 TB. The 8 GB tier wins both.

Monthly equivalents, if you prefer to think that way: about **$1.83, $3.00, $5.00, $7.50 and $10.00 per month**. All of those are derived from the annual prices, because this page does not sell monthly billing.

## Do RackNerd renewals go up?

No, according to RackNerd's FAQ, which states that these VPS specials are lifetime recurring and renew "at the same rate for as long as you decide to keep the service." There is no separate regular price listed next to the special price, because the number on the page is the special and the renewal.

That matters more than it sounds. Year two costs $59.99 on the 4 GB plan, and year three costs $59.99 again. A three-year total is simply three times the annual price, which is a predictable number you can put in a budget instead of a first-term discount that resets upward at renewal.

## What can you do in ctrl without opening a ticket?

ctrl is RackNerd's own panel, bundled with every VPS on this page, and it covers the routine work that otherwise turns into a support thread.

Power control, reboot and rescue mode sit on one screen, with confirmation prompts before anything destructive. The HTML5 VNC console is out-of-band, so it works when SSH doesn't, which is what makes it useful for recovery, troubleshooting and installing an OS from your own media. OS reinstalls, root password resets, hostname changes and network reconfiguration are self-service. An optional inbound firewall filters traffic in front of the VPS with rules you manage in the panel. Memory, disk and bandwidth meters show how close you are to the limits, and upgrades are handled there too.

The panel also supports two-factor authentication; RackNerd published a walkthrough for enabling it in November 2026, plus a separate video on booting into rescue mode through ctrl. There is a public interactive demo that needs no account if you want to click through the interface before buying.

None of this changes the support model. The VPS is unmanaged, full root SSH stays available at all times, and 24/7 support covers the platform itself rather than your application configuration.

👉 [Compare the five plans and pick your RAM tier](https://bit.ly/RacKnerd)

## Where the VPS sits: Los Angeles DC-03

RackNerd runs multiple locations, and the one with public detail is Los Angeles DC-03 at 1200 W 7th St., downtown LA. The facility connects through Cogent and Arelion, holds SOC2 and SSAE16 certifications, and carries 24/7 on-site staffing. RackNerd added rack space there in 2025 to meet Los Angeles demand and positions the site for compute-heavy workloads, including AI and LLM deployments. To land on it, select "Los Angeles DC03" as your location during checkout; the choice is made at order time, so decide before you pay rather than after.

If your users are not on the US West Coast, pick the location nearest them instead. Latency is the one thing you cannot fix later without migrating.

## Who shouldn't buy a RackNerd VPS special?

**Anyone who wants a managed server.** Nobody will configure your stack, patch your apps or debug your container networking for $59.99 a year. Support handles the host, the network and the panel; the software on top is yours.

**Anyone who wants cPanel shared hosting.** This is a bare KVM VPS, not a hosting account with a support team that fixes WordPress plugins for you.

**Anyone who needs more than one IPv4, Windows, or IPv6.** Every plan lists one IPv4 address and a Linux distribution set. Windows does not appear among the install options, and IPv6 is not mentioned on the plan pages. Ask support before ordering if any of those are requirements.

**Anyone who expects a refund.** RackNerd's knowledge base is direct about it: "Per our terms of service, we do not offer refunds or have a money back guarantee." The annual fee is committed once paid, so match the plan to your workload before checkout and keep your own off-server backups from day one.

One more gap worth naming: the plan pages do not describe what happens when you exceed the monthly transfer allowance. If your workload will run near 3 TB or 7 TB, confirm the overage policy with support first.

## Picking your tier in one pass

- A static site, reverse proxy, jump box or one light container: **1 GB, $21.99/year**.
- n8n, Coolify, Docker with Portainer and a few services: **2 GB, $35.99/year**.
- Ollama, LibreChat, AnythingLLM or Hermes Agent: **4 GB, $59.99/year**.
- OpenClaw, or several models and a chat UI on one machine: **8 GB, $119.99/year**, which also buys the most SSD and transfer per dollar in the lineup.

Two things to settle at checkout. First, the location: choose the datacenter closest to your users, or "Los Angeles DC03" if that is the one you want. Second, the RAM floor of the app you plan to run, since every tier below it is money spent on a server that will struggle with the job you bought it for. Get those two right and the annual price you see today is the annual price you renew at.

👉 [Order the RackNerd VPS plan that matches your workload](https://bit.ly/RacKnerd)
