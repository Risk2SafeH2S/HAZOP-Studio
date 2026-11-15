---
title: "Peer Review – HAZOP Node 1 (V-301 / V-100 to V-312 via ST-017 A/B)"
subtitle: "Review of 'Hot Oil Unit HAZOP Worksheet – Node 1 completed – 10 Nov 2026'"
date: "11 Nov 2026"
---

# 1. Overall verdict

**Do not approve Node 1 for closure yet. Record it as OPEN with formal hold points.**

The worksheet is better than average:

- It does not credit the non-functional V-301 trips, the LCP or PSV-304B.
- It caught the LSHH/LSLL tag transposition and the V-100 free-water routing to V-312.
- It replaced "overpressure not credible" with an API 521 action (Rec 3) and a LOPA (Rec 14).

However, five independent reviewers found the following problems:

- **Undefined pressure basis.** The study is marked "completed", but the pressure and relief basis that every gas blow-by and overpressure ranking depends on is not defined.
- **Missed paths to V-312.** Several credible high-pressure-to-low-pressure and bypass paths into V-312 on the P&IDs were missed.
- **Unproven safeguards.** Some safeguards are credited even though they do not exist on the drawings, cannot be proven, or point the wrong way.
- **Unsupported residual risk.** Residual risk for the main scenario is claimed against recommendations that are conditional or deferred.

Review method: 5 specialist reviewers worked in parallel on these lenses:

1. Methodology and completeness
2. P&ID cross-check
3. Safeguards against field condition
4. Overpressure and relief
5. Risk ranking and recommendations

Findings raised by more than one reviewer are marked **[×n]**. The detailed register from each reviewer is in the Appendix (83 raw findings before de-duplication).

# 2. Consolidated critical / major findings

| # | Finding | Worksheet ref | Raised by | Required action |
|---|---|---|---|---|
| C1 | **The study is closed on an undefined pressure basis.** Open items: well 192B CITHP, V-301 operating and design pressure, V-301 PSV set pressure, ST-017 rating, V-312 relief device and discharge, H2S content, the cold-vent dispersion study (HOLD 1 on 041/025) and the flushing-mode node ("Node 3 – to be added"). | Header; Dev 2, 5, 10, 13, 19 | Overpressure, Risk **[×2]** | Re-issue as "Open – hold points". Make each TBC/INPUT REQUIRED a numbered hold point before the trial. Re-rank Dev 2, 5, 10 and 13 when the data is available. |
| C2 | **There is no V-312 relief device on P&ID 041, yet "V-312 PSV" is credited for gas blow-by.** The items next to LSHH/LSLL-1004 are PSD functions. V-312 relies on the 2" cold vent (Note 5). Rec 4 would also blind the line to the LAM-16 flare, which may be the only other outlet. | Dev 2 sg 2; Dev 10, 13; Rec 4 | Safeguards, Overpressure, Risk **[×3]** | Remove the credit. Confirm the V-312 relief path and size it for gas blow-by and fire (API 521). Check that Rec 4 does not isolate a relief path. Assess the capacity and dispersion of the 2" vent (outlet about 3 m). |
| C3 | **The 150# B013 section can be overpressured by blocked-in liquid** and has no relief. Closing the ST-017 outlet or the V-312 inlet (BV-352) while (022) or the V-100 outlet is open settles the 3" line and ST-017 out at separator pressure. The C013/B013 break at TP-04 and the D013/B013 break at TP-01A/B are unprotected. There is no thermal relief on blocked-in liquid between the DBB valves or at ST-017. | Dev 1 cause 1; Dev 5; Dev 7; Rec 3 | Methodology, P&ID, Overpressure **[×3]** | Add these as causes and rank them. Extend Rec 3 to cover blocked outlet, thermal expansion and the fire case for the B013 section and ST-017. Provide a PSV or TSV, or a full-rating spec break. |
| C4 | **An existing V-301 to V-312 line bypasses ST-017 and the new 150# section.** P&ID 031 shows 4"-PR-C013-155-X "TO BULLET TANK" (via FSV-010 / BV-023 / (024)), which arrives at V-312 N5 on P&ID 041. The V-301 header also reaches the oil heater (6"-PR-C013-152-X). Neither is in Dev 4 or in the Rec 4 blind list. | Dev 4; Rec 4; Dev 11 | Methodology, P&ID, Overpressure **[×3]** | Add to Dev 4 (mis-direction, blow-by, unfiltered sand). Positively isolate with blinds and add to the blind register. |
| C5 | **The NC manual bypass (017) around LV-303 is not addressed.** It is a direct gas blow-by path into the B013 section that does not pass through LV-303. The NC bypass (016) around PV-303 is also missing. | Dev 2, 5, 10; Rec 2, 3, 11 | P&ID **[×1 – verify on 031]** | Add as a cause. Lock or car-seal it closed, and include it in the line-up and blind checks. |
| M1 | **The V-100 route is missing from the gas blow-by and HP/LP analysis.** V-100 has a DP of 55 barg and operates "close to wellhead choke downstream pressure" (030 Note 5). It feeds the same 150# line through only a manual valve and a check valve. Rec 3 lists only CITHP and BV-018, and Rec 10 does not require the calculation. | Dev 2, 5, 10; Rec 3, 10 | Methodology, P&ID, Overpressure **[×3]** | Add V-100 low level and LV-102B/LCV-304 failing open as causes. Include V-100 and the Block-1 trunkline (600#) in Rec 3, or make exclusion of the V-100 route a firm precondition. |
| M2 | **The check valve is credited in the wrong direction.** The TP-01A/B trunkline connection is upstream of the check valve on 3"-PR-B013-8086-H, so it passes flow towards ST-017. In any case, a check valve is not an acceptable overpressure layer under API 521. | Dev 4 cause 2/3; Dev 3 | P&ID, Safeguards, Overpressure **[×3]** | Remove the credit and re-rank. Treat it as an HP/LP interface under Rec 3. |
| M3 | **Residual risk for the main blow-by scenario is not supported.** It drops from C4 RR2 to C2 RR3 on the basis of Rec 3 (conditional), Rec 2 (escape clause: "or record that no shutdown function exists") and Rec 14 (LOPA not yet done). LSLL-305 also has no defined final element and no independence from LV-303/LIC-302. | Dev 2, 10 (residual); Rec 2, 3, 14 | Safeguards, Risk **[×2]** | Keep the residual at current risk until the LOPA is complete. Delete the escape clause from Rec 2. Specify an independent trip with a defined final element and verify its SIL. |
| M4 | **PSV-304A is credited without auditable evidence.** There is no set pressure, V-301 DP, test record or locked-open block valves. The open nozzle and isolation valve left by the removed PSV-304B are not addressed. | Dev 1, 4, 5, 13; Rec 9 | P&ID, Safeguards, Overpressure, Risk **[×4]** | Provide test/calibration records and confirm block valves are CSO or LO, or remove the credit. Blind or isolate the PSV-304B position. |
| M5 | **Some safeguards are inconsistent or defeated by their own cause:** <br>- "Strainer bypass locked closed" is defeated by the strainer-blockage cause, and contradicts Dev 17 ("bypass allows isolation"). <br>- A corroded V-100 level gauge is credited. <br>- "Integrity inspection programme" is credited even though it has failed (severe corrosion observed). <br>- "NC valve philosophy Note 7" refers to the wrong drawing and note, and no valves are locked. <br>- LG-301 and LIC-302 share a common bridle, so they can fail from a common cause. | Dev 1, 3, 4, 17, 18; Dev 9 | P&ID, Safeguards **[×2]** | Remove the invalid credits and re-rank. Raise the Dev 18 likelihood. |
| M6 | **Likelihood is inconsistent for the same consequence.** IA loss leading to LV-303 failing open is ranked L3 (Dev 13), while Dev 2 and 10 are L4. The V-100 route is ranked lower than V-301 although it has fewer working barriers. Dev 9 and Dev 10 get different reductions for the same recommendation. | Dev 1.4, 9, 10, 13 | Safeguards, Risk **[×2]** | Calibrate the rows against each other and re-rank. |
| M7 | **Severity is understated for gas blow-by, fire and explosion** (People C, Asset D, Reputation E) and for burning-liquid fall-out (People D). Residual severity is lowered by preventive recommendations in Dev 11.1 and Dev 4.1, which is a methodology error. | Dev 1.2, 2, 4.1, 9, 10, 11.1 | Methodology, Risk **[×2]** | Rank severity on the worst credible outcome. Change severity only through mitigation of the consequence. |
| M8 | **Operator response is credited (5 min) with no process safety time.** Detection relies only on local PIs read every 10 min, which is too slow for gas blow-by. "Close well 192B choke" is a remote action. | Rec 11; Dev 1.2, 2, 9, 10, 12 | Safeguards, Risk **[×2]** | Establish the process safety time. Credit operator response only if detection plus action fits inside it. Otherwise provide automated protection. |
| M9 | **The LOPA/SIL scope is too narrow.** There are six People-C RR2 scenarios, but Rec 14 covers only Dev 2 and 10. | Rec 14; Dev 4.1, 5, 11, 12 | Risk | Extend the LOPA to all RR2 and People-C scenarios. |
| M10 | **Reverse flow from Node 2 and V-312 is not analysed.** The P-003 minimum-recirculation line (2"-PR-B013-8094-H) joins the Node 1 outlet, and 3"-8085-H has no check valve. Hot oil (75–80 °C) or V-312 gas could reach an open ST-017 during cleaning. | Dev 3, 7 | Methodology, Overpressure **[×2]** | Add as causes. Provide isolation or a check valve, and address this in the strainer-cleaning procedure. |
| M11 | **Flashing, two-phase flow, JT cooling and static are dismissed.** Crude flashes across LV-303 or LCV-304 into a near-atmospheric tank. Blow-by gas cools below -29 °C. Air ingress on the atmospheric vent can give a flammable vapour space during splash filling. Nitrogen connection TP-07 is not used. | Dev 8, 11, 15; Dev 4 | Methodology, Overpressure **[×2]** | Add these deviations. Consider N2 blanketing, bottom or dip-pipe filling, and bonding of ST-017. |
| M12 | **The V-301 water draw-off (N9, valve 102) ties into the oil outlet upstream of LV-303,** so free water reaches V-312 through Node 1. The V-100 water and oil routing highlighted on 030 is ambiguous. | Dev 4.1, 11, 16; Rec 5 | P&ID | Clarify on the drawings and add as a cause. |
| M13 | **Other systems are tied into V-312 and its vent:** a direct wellhead line, LP separator, PSV discharges, the open-drain tank vent, and V-001 at TP-12A/B. Blow-by into V-312 can back-pressure the vent and push gas into V-001 and the open-drain header. | Dev 2 cons. 2; Dev 4 | P&ID, Overpressure **[×2]** | Assess this in Node 1, or explicitly in Node 2 with a cross-reference. |
| M14 | **Sour service is not checked.** Well 192B H2S content is unknown, but no action checks the B013 lines, valves, gaskets, bolting or the ex-stock ST-017 against NACE MR0175 / ISO 15156. H2S severity is inconsistent between rows and there is no detection action. | Dev 11.3, 14, 16, 18; Rec 7 | Overpressure, Risk **[×2]** | Make H2S data a pre-trial hold point. Add a materials check, personal and fixed H2S detection, and re-rank. |
| M15 | **The Hot Oil Unit condition report is not used.** The worksheet ignores it although Node 1 consequences end in the HOU. The report shows failed heater protections and failed ignition-source isolation (ESD and engine air shut-off). | Header condition basis; Dev 1.3, 4.1, 11, 15 | Safeguards | Add the report to the condition basis. Make HOU protections a hold point, or analyse them in Node 2. |
| M16 | **The node boundary and design intent are not defined.** The P&ID highlight starts at TP-04 and colours 3"-8085-H (V-312 inlet) as Node 2, while the worksheet analyses V-301 internals. The worksheet gives no flow, batch size, operating mode or operating pressure. | Header | Methodology | Write a design intent statement and align the markups with the worksheet. |
| M17 | **Recommendations lack owners, dates and priorities.** Only Recs 2, 3 and 13 have timing. There are joint owners, and Rec 1 bundles five or more actions. No recommendation asks for V-301 design data, the MOC number, or a leak or pressure test of the new 3" lines. | All Recs; Responsibility column | Risk **[×2]** | Make every recommendation SMART with one owner and a due date or hold point. Split Rec 1. Add the missing pre-start-up actions. |

# 3. Minor / documentation issues (summary)

**Document control**
- The title says "Hot Oil Unit HAZOP" but the content covers crude transfer.
- The document carries three different dates.
- There is no revision status, attendance list or MOC number.
- A leftover row of placeholder data sits in the blank Node 2 table.
- Consequence numbering repeats.

**Tag and line defects**
- PI-54X is a placeholder tag, and PI-545 appears on both 031 and 041.
- 3"-PR-B013-8087-H is used for two lines.
- Off-page connectors do not match.
- Some V-100 tags conflict with the inspection sheet.
- LCV-304 may not be on the highlighted path.
- ST-017 is titled "A/B" but is drawn as a single basket.

**Unchecked line codes**
- The new lines end in "-H", which may be an insulation or tracing code. This would contradict the Dev 8 statement "no tracing/insulation shown". The legend sheets were not provided.

**Equipment origin**
- V-301 carries LAM-75 tags. It may have been relocated, so verify its nameplate, certification and as-built DP.

**Scope gaps**
- Start-up/shutdown covers only operator unfamiliarity. First hydrocarbon introduction and end-of-batch are not covered.
- V-312 high level is never analysed although Node 1 is its filling source.
- Fire & gas detection and executive action are not considered.

**Ranking columns**
- Environment and Reputation are almost always E/F, which suggests they were not assessed on their own merits.
- There is no ALARP statement for the residual RR3 People-C scenarios.

# 4. Strengths acknowledged

- The ranking basis is explicit and applied consistently: untested items are not credited, the 6×6 RAM is used, and every S/L to RR lookup is arithmetically correct (all 200 triplets checked).
- The study caught the LSHH-304/LSLL-305 tag transposition between the inspection sheet and the P&ID.
- It identified the V-100 free-water routing to V-312, and that ST-017 is drawn as a single basket with a bypass.
- It requires positive isolation of the other V-301 inlets (BV-018, BV-019, coflex, LP gas), with a blind register.
- It treats human factors in an all-manual line-up realistically.
- It covers wax, IA failure, strainer cleaning, drainage and sampling.
- Missing inputs are stated openly instead of assumed.

# 5. Recommended next steps

1. Re-issue the worksheet as **Rev B – Open**, with a hold-point register covering C1 and M14/M15.
2. Hold a short HAZOP revalidation session (Node 1 + Node 2 boundary) to add the missed causes C3, C4, C5, M1, M10, M11, M12 and M13, and to re-rank after removing the invalid safeguard credits (C2, M2, M4, M5).
3. Freeze the residual rankings for Dev 2, 5, 10 and 13 until the Rec 3 API 521 calculation and an extended LOPA (M9) are complete.
4. Make all recommendations SMART, with single owners and pre-start-up flags.

# Appendix – Individual reviewer registers


## A1. Methodology, node definition & completeness

**Reviewer summary.** Lens: methodology, node definition and completeness. The Node 1 worksheet is better than average. It deliberately takes no credit for the untested Repco and TDE protections, and it covers most of the standard guidewords. Its recommendations target the HP/LP interface, positive isolation and the SOP.

The node is still not complete enough to approve the trial, for three reasons:
1. The node boundary and design intent are not defined. The worksheet node runs from V-301/V-100 to V-312. The marked-up P&IDs start the Node 1 highlight at TP-04 and give the V-312 inlet line 3"-PR-B013-8085-H the Node 2 colour.
2. Several credible high-consequence causes visible on the P&IDs are missing:
   - The V-100 high-pressure source (DP 55 barg; P&ID 030 Note 5) is not included in the HP/LP blow-by analysis or in Rec 3.
   - The 150# section can be blocked in downstream of ST-017. The study does not cover the resulting overpressure or thermal expansion.
   - An existing un-strained V-301 to V-312 line (4"-PR-C013-155-X, entering V-312 at N5 behind a single NC valve) is not covered.
   - The P-003 minimum-recirculation line (2"-PR-B013-8094-H, Note 3) joins the Node 1 outlet line, which creates a possible reverse flow of hot oil. This is not analysed.
   - Live crude flashes into the atmospheric V-312 during normal operation, and filling may cause static charge. Neither is analysed.
3. High temperature, overfill, vent and heater effects are referred to Node 2 (blank) and a 'Node 3 (to be added)' that does not exist.

Document control is weak. The document is titled 'Hot Oil Unit HAZOP' but covers crude transfer, and it carries three different dates. It has no revision status, attendance list or MOC number. A leftover row of placeholder data sits in the blank Node 2 template.

Ranking: 6 Major, 7 Minor and 3 Observations. No single finding is Critical, because the study already blocks credit for the unproven protections and requires the Rec 2, 3 and 4 closures before the trial.

**Strengths noted:**

- The ranking basis is stated explicitly: current risk takes no credit for non-functional or untested items, residual risk is after recommendations, and the DO 6x6 RAM is used. It is applied consistently. LSHH-304, LSLL-305, the LCP and PSV-304B are all marked NOT CREDITED, in line with the Repco inspection sheet items 1-3 and 8.
- The tag transposition was caught: the Repco inspection sheet gives LSHH-305 and LSLL-304, while P&ID 031 shows LSHH-304 and LSLL-305. Rec 2 records this.
- The free-water drain mis-routing was found: P&ID 030 Note 3 sends V-100 water to the 'LLP header [to Bullet Tank-C]' 4"-PR-D013-5076-X, which ends in V-312 (Deviation 4, Rec 5).
- Gas blow-by from V-301 through LV-303 into the 150# line, ST-017 and V-312 (DP 20 barg) is identified as the principal scenario. The draft statement 'overpressure not credible' is replaced by a required API 521 calculation (Rec 3) and a LOPA (Rec 14).
- Other inlets to V-301 are identified as uncontrolled: BV-018 HP header, BV-019, coflex lines and the LP-separator gas lines (P&ID 031). Rec 4 requires positive isolation by blinds with a blind register.
- The study notes that P&ID 031 draws ST-017 as a single basket with a 100% LC bypass, although it is titled 'A/B' (Rec 6). It also states that the bypass must not be used with the heater lit.
- Human factors in an all-manual line-up are treated realistically. L4 is kept until blinds and two-person verification are in place, with Recs 1, 11 and 13 and a manning and stop-action regime.
- Low-temperature wax plugging between batches, IA failure with unverified fail positions, strainer cleaning, drainage and sampling are all covered as separate deviations.
- Missing inputs (well 192B CITHP, V-301 design data, MOC number) are stated openly instead of assumed.


### A1.1 [Major] The node boundary and design intent are not defined, and the worksheet scope does not match the marked-up P&IDs.

- **Worksheet ref:** Node 1 header (design intent / boundary); P&ID 031 and 041 markups
- **Evidence:** The worksheet node title runs 'from V-301 or V-100 to V-312' and analyses V-301 internals (high and low level, PV-303, PSV-304A/B). On P&ID 031 (page 1), the purple Node 1 highlight starts at TP-04 downstream of manual valve (022) and does not include V-301, LV-303 or the (020)/(021)/(022) line-up. On P&ID 041 (page 3), the V-312 inlet 3"-PR-B013-8085-H from ST-017 to TP-06A/N1 is highlighted in the Node 2 colour. The header gives no design intent statement: no transfer rate, batch volume, operating mode (filling vs flushing) or normal V-301/V-312 operating pressure (OP = 'TBC').
- **Recommendation:** Write a design intent statement for Node 1: source vessel, route, flow and batch size, normal and maximum pressure and temperature, and operating mode. Redraw the node highlight so it matches what was analysed (start at the V-301 and V-100 liquid outlet nozzles and end at V-312 nozzle N1), or move the V-301 vessel deviations into their own node. Reconcile the boundary with Node 2 so that no section is analysed twice or missed.


### A1.2 [Major] The HP/LP interface and gas blow-by analysis covers only V-301. The V-100 route also has a high-pressure source feeding the same 150# line, and it is not analysed.

- **Worksheet ref:** Dev 2 More Flow, Dev 5 High Pressure, Dev 10 Low Level; Rec 3
- **Evidence:** P&ID 030 Note 5 says 'Test separator shall be operated close to the wellhead choke valve downstream pressure'. The worksheet header gives V-100 DP as 55 barg. The V-100 route (page 2) runs from 2"-600# and 3"-600# piping (TP-02A/B, TP-01A/B, DBB PI-543) into 3"-PR-B013-8086-H 150# to ST-017. Only a check valve and a manual valve sit at the spec break, and there is no PSV. Dev 2 lists 'LCV-304 wide open' only as an overfill (more flow) cause. Dev 10 Low Level covers V-301 only. Rec 3 lists only 'well 192B CITHP and HP-header pressure through BV-018'. The worksheet does not state how high V-100 pressure can rise.
- **Recommendation:** Add V-100 low level and LV-102B/LCV-304 failing open (gas blow-by) as causes under Low Level and More Flow. Extend Rec 3 to cover V-100 maximum operating pressure (up to the wellhead choke downstream pressure and its 55 barg DP) against the 150# rating. Alternatively, make Rec 10 (exclude the V-100 route) a firm precondition and not an option.


### A1.3 [Major] The new 150# section can be blocked in, causing overpressure, and liquid trapped between closed valves can expand thermally. Neither is analysed as a cause or consequence for the Node 1 piping.

- **Worksheet ref:** Dev 1 No/Less Flow, Dev 5 High Pressure, Dev 7 High Temperature
- **Evidence:** Dev 1 consequences cover only V-301 level and pressure rising. Dev 5 causes cover only PV-303 and the HP header. Neither lists closure of the ST-017 outlet valve, the V-312 inlet valve (TP-06A/BV-352 area, P&ID 041) or a blocked strainer as exposing 3"-PR-B013-8083/8085-H and ST-017 (rating 'TBC') to full V-301 or V-100 pressure. Dev 7 is dismissed with 'No heat source in Node 1'. Solar heating of crude trapped between the manual and DBB valves on the 3" lines and ST-017 is not considered, and no thermal relief valve is shown on page 1. Rec 3 mentions 'blocked-outlet cases per API 521' only in general terms.
- **Recommendation:** Add the following causes: 'closure of the downstream valve (ST-017 outlet, V-312 inlet) with the upstream line open' under High Pressure, and 'blocked-in liquid with solar or ambient heating' under High Temperature/Pressure. Rank them. Make Rec 3 explicitly cover the blocked-in 150# segment and the need for thermal relief, and confirm the ST-017 design pressure.


### A1.4 [Major] Existing parallel outlets from V-301 are left out of the misdirected-flow analysis and the isolation list. These include an existing V-301 to V-312 line that bypasses ST-017 and the new 150# section.

- **Worksheet ref:** Dev 4 Mis-directed Flow; Rec 4 (blind list)
- **Evidence:** P&ID 031 (page 1) shows V-301 liquid also routed 'TO OIL HEATER 6"-PR-C013-152-X' through FSV-010/BV-023 and 'TO BULLET TANK 4"-PR-C013-155-X'. P&ID 041 (page 3) shows this line arriving as 'FROM REPCO SEPARATOR 4"-PR-B013-155X3' at V-312 nozzle N5. It is isolated only by a 3",600# BV-XXX marked NC. Dev 4 and Rec 4 do not mention these lines. Rec 4 lists only BV-018/019, the V-100 trunklines, TP-01/02/03 and the flare line.
- **Recommendation:** Add these as causes under Mis-directed Flow and Reverse Flow: an open existing V-301 to V-312 line (unfiltered sand, uncontrolled fill, gas blow-by path not covered by the 150# calculation), and V-301 liquid to the oil heater line. Add both lines to the Rec 4 blind register.


### A1.5 [Major] Reverse flow from the Node 2 side into Node 1 is not analysed. Hot oil from the P-003 minimum-recirculation line could reach the Node 1 outlet line.

- **Worksheet ref:** Dev 3 Reverse Flow; Dev 7 High Temperature
- **Evidence:** On P&ID 041 (page 3), '2"-PR-B013-8094-H NOTE-3' (Note 3: 'Min recirculation line for pump protection') runs from the P-003 discharge (P-003 discharge pressure 6 barg, datasheet on page 3) and appears to join 3"-PR-B013-8085-H upstream of the V-312 inlet. Per P&ID 062 Note 5, oil is heated to 75-80 C. No check valve is visible on 8085-H between the tee and ST-017. Dev 3 considers only V-301 against V-100. Dev 7 dismisses high temperature as 'Not credible in filling mode' and defers the flushing mode to 'Node 3 (to be added)', which does not exist in the document.
- **Recommendation:** Confirm on the P&ID where the recirculation line ties in and whether a check valve is fitted. Add the cause 'P-003 recirculation / V-312 back-flow into the ST-017 line when V-301 or V-100 pressure is low or the line-up is wrong', with the consequences: hot oil into the strainer and drains, and back-flow to the separators. Analyse the flushing return mode as a defined node before approval, instead of deferring it.


### A1.6 [Major] Flashing of live crude into the atmospheric V-312 during normal operation, and static from splash filling or flow through the strainer, are not covered. Both are dismissed as Node 2 issues or as no incremental concern.

- **Worksheet ref:** Dev 11 Composition; Dev 15 Ignition/Static
- **Evidence:** Dev 11 covers sand, water and H2S but not dissolved gas or GOR. V-301 operates at separator pressure while V-312 is vented to atmosphere (P&ID 041 Note 5). The flash gas load at the vent therefore originates in Node 1 even without blow-by. P&ID 030 Note 2 asks only for 'min gas', with no limit. Dev 15 says 'no new ignition source in Node 1; the new release point (V-312 vent) is in Node 2'. The inlet 8085-H enters at nozzle N1 through TP-06A, and no dip pipe is visible on page 3. Static from flow through the ST-017 basket and from splash filling is not discussed.
- **Recommendation:** Add 'More Composition – dissolved gas / flash from V-301 pressure to atmospheric' with a quantified flash rate, and pass it to the Node 2 vent dispersion (HOLD 1 on P&ID 041/025). Add static accumulation from splash filling and strainer flow, covering velocity limits, a dip pipe or bottom entry, and bonding. Include a gas or RVP limit in the Rec 7 acceptance criteria.


### A1.7 [Minor] The Start-up/Shutdown deviation covers only operator unfamiliarity. It does not cover first introduction of hydrocarbons into new piping, or the end of a batch.

- **Worksheet ref:** Dev 12 Start-up/Shutdown
- **Evidence:** Dev 12 cause: 'Operations team not familiar with the new set-up...'. The study does not cover:
- leak or tightness testing of the new tie-ins TP-01A/B, TP-02A/B, TP-03, TP-04 and TP-06A/B
- removing hydrotest water from the new 3" lines, which links to the steam-flash consequence in Dev 4
- purging air or oxygen before crude is introduced into the line and V-312
- emergency shutdown of a transfer, given that there is no ESD on V-301 or V-100
Batch end-of-transfer and the low-level stop are covered only through Rec 11.
- **Recommendation:** Split Dev 12 into first start-up (commissioning of new piping: leak test, dewater, purge, PSSR), normal batch start, batch stop, and emergency stop. Develop the causes and consequences for each.


### A1.8 [Minor] Auto-refrigeration and low-temperature embrittlement during depressurisation or gas blow-by across LV-303 or LCV-304 is missing.

- **Worksheet ref:** Dev 8 Low Temperature
- **Evidence:** Dev 8 covers only ambient cooling and wax. The header DT is '-29 to 110 C (V-312 governs)' and the new lines are CS B013. Gas blow-by (Dev 2/10) from V-301 or V-100 pressure to near-atmospheric V-312 causes Joule-Thomson cooling. Its effect on the minimum design metal temperature of the 3" lines and ST-017 is not considered.
- **Recommendation:** Add a Low Temperature cause: JT cooling on blow-by or depressuring. Confirm the minimum design metal temperature as part of Rec 3.


### A1.9 [Minor] Key consequences are referred to Node 2, which is blank. V-312 high level is never analysed in Node 1 even though Node 1 is the filling source.

- **Worksheet ref:** Dev 9 High Level, Dev 1, Dev 2; Node 2
- **Evidence:** Dev 2 consequence 1 says 'V-312 fills rapidly (overfill - see Node 2 high level)'. Dev 11 says 'see Node 2 composition'. Dev 15 says 'V-312 vent is in Node 2'. The Node 2 table in the same document contains only an empty template (OT/OP/DT/DP blank). P&ID 041 shows that V-312 has many other inlets (new LLP header, LP separator 21-V-302, interim bullet tank, wells 120/137, vent drain drum V-001). Simultaneous inflow from these would affect Node 1 overfill.
- **Recommendation:** Either analyse V-312 high level as a Node 1 consequence (cause: transfer not stopped, LSHH-1004 / LT-1004 status, other inlets open), or complete Node 2 before issuing Node 1 and cross-reference it explicitly. Add the other V-312 inlets to the Rec 4 isolation list.


### A1.10 [Minor] The same scenario is counted under several deviations, each ranked People C4 RR2, which inflates the risk profile and blurs traceability.

- **Worksheet ref:** Dev 2 cause 1 vs Dev 10 cause 1; Dev 13; Dev 5 second row
- **Evidence:** Dev 2 cause 1 'LV-303 fails open / LIC-302 mis-set... GAS BLOW-BY' and Dev 10 cause 1 'LV-303 stuck open / LIC-302 fails open; V-301 liquid level lost' are the same event with the same ranking (C/4/RR2) and the same recommendations (Recs 2, 3, 14). Dev 13 repeats it again ('Fail-open LV: gas blow-by (deviation 10)') and ranks it C3. Dev 5 contains an unranked row that only cross-refers to Dev 2 and 10. The ranking of 'Inadvertent closure' under Dev 1 also repeats Dev 12.
- **Recommendation:** Rank each initiating event once, in its primary deviation. Elsewhere, use 'refer to Dev X' without a separate ranking. Keep the IA-loss row only for the common-cause effect (several valves failing at once).


### A1.11 [Minor] Some consequences stop short of the worst credible outcome, and residual risk is claimed before the controlling calculation exists.

- **Worksheet ref:** Dev 2, Dev 10, Dev 4 (variant), Dev 12, Dev 19 – severity column
- **Evidence:** The gas blow-by consequence reads 'overpressure of the LP section and / or large gas flow out of the atmospheric vent stack; LOPC, fire / explosion'. It is ranked People C. Rupture of V-312 (DP 20 barg, vented to atmosphere) or ignition of a vapour cloud on a manned platform is not developed and could warrant a more severe category. The DO RAM definitions are not attached, so this cannot be verified. The Dev 2/10 residual is C2 RR3 on the strength of Rec 3, which is a calculation and not a barrier, and Rec 14, a future LOPA.
- **Recommendation:** Write the worst credible outcome explicitly (for example vessel rupture, jet fire or VCE, with the number of people exposed). Attach the RAM severity definitions. Mark the residual risk for the blow-by scenarios as 'to be confirmed after Rec 3 / Rec 14' instead of assigning L2.


### A1.12 [Minor] Document control is not to issue standard. The title does not match the content, dates conflict, and revision, attendance and MOC details are missing.

- **Worksheet ref:** Document header/footer, file name, docProps
- **Evidence:** The file is named 'Hot_Oil_Unit_HAZOP_Worksheet-Node_1_completed-10_Nov_2026'. The header reads 'Dragon Oil / HAZOP Study / Printed On: 11/4/2026'. The footer reads 'File Name: LAM 28 HOU HAZOP Worksheet 27 Oct 2026'. The document properties title is 'Document 1'. Node 1 covers crude transfer from the separators to V-312, not the Hot Oil Unit, and the project title on the P&IDs is 'Replacement of diesel with stabilized crude oil for hot oil flushing in LAM-28'. The document has no document number, revision or status, HAZOP session dates, team attendance or roles, or MOC number. Dev 19 itself states 'MOC number' is still required.
- **Recommendation:** Retitle the document to the project scope and give it a controlled number, revision and status. Use one consistent session date. Add the team attendance sheet, the terms of reference, the P&ID list with revisions, the MOC number and a recommendation register.


### A1.13 [Minor] There are template and formatting defects: a leftover row of data in the blank Node 2 table, repeated consequence numbering, and a non-deviation used as a catch-all.

- **Worksheet ref:** Node 2 table; Dev 1 numbering; Dev 19
- **Evidence:** The Node 2 table contains placeholder data with no parameter or deviation text ('Flow ... E 4 Engineering E 4 C 4 E 4 D 4 F 4 Engineering C 4 ...'). In Dev 1, cause 1 has two consequence entries both numbered '1.' ('Inability to supply...' and 'Blocked outlet...'). Dev 19 'Any Other Safety Issue' lists missing design data and the commissioning status of the protection system, which are study-basis gaps. It is ranked C4 RR2 as though it were a hazard scenario.
- **Recommendation:** Delete the stray Node 2 row. Number consequences uniquely so each recommendation can be traced. Move the Dev 19 content into a 'study basis / holds' section and leave it unranked.


### A1.14 [Observation] Spec breaks and line numbers on the drawings do not match the worksheet's simple '150#' basis.

- **Worksheet ref:** Header DP; P&ID 031 near TP-04; P&ID 030/031 line numbers
- **Evidence:** P&ID 031 shows '3"-300#' and a C013|B013 spec break immediately after TP-04, on 3"-PR-B013-8083-H. P&ID 030 shows 2"-600# and 3"-600# on the V-100 tie-in before 8086-H at 150#. The line number '3"-PR-B013-8087-H' appears both on P&ID 031 (ST-017 bypass) and on P&ID 030 (at PI-544 / TP-02A/B). The strainer downstream gauge is tagged 'PI-54X', an unassigned tag. The worksheet header lists only 'new 3"-B013 lines 150#'.
- **Recommendation:** Have the Rec 3 calculation state each spec-break location and the rating of each segment. Ask Engineering to resolve the duplicate line number and assign the PI-54X tag before IFC.


### A1.15 [Observation] The trial basis depends on fluid quality notes on the P&IDs that have no numeric limits. The worksheet notes this but still ranks sand at C4 with sampling credited as a safeguard.

- **Worksheet ref:** Dev 11 / Rec 7 / Remarks
- **Evidence:** P&ID 030 Notes 2 and 4 say the fluid shall be 'free of sand, min gas & water' and analysed. Dev 11 credits 'Periodic sampling... frequency and limits not defined' as a procedural safeguard.
- **Recommendation:** Do not credit sampling as a safeguard in current risk until Rec 7 sets the limits and the release authority.


### A1.16 [Observation] Some instruments on the V-100 inspection sheet are not used in the study, and some in the study cannot be checked against it.

- **Worksheet ref:** Inspection sheets vs worksheet coverage
- **Evidence:** The TDE sheet covers LCV-304, LV-102B, LC-101B, PCV-100B, the IA manifold, PSV-100B and the level gauge. It does not inspect LSHH, LSH or LSLL-101B. Dev 1 cause 3 cites 'LV-101B', which does not appear on the inspection sheet; I could not verify it legibly on P&ID 030. The hot oil unit condition report (burner and engine LCP ESD buttons failed, damaged low-flow switch) relates to Node 2 and is not referenced in Node 1. That is acceptable, but it confirms Node 2 must be completed before the trial.
- **Recommendation:** Check the LV-101B tag against P&ID 030. Carry the hot oil unit condition report findings forward explicitly into Node 2.


## A2. P&ID cross-check

**Reviewer summary.** P&ID cross-check of the Node 1 HAZOP worksheet against all 5 marked-up drawings: 031-00 Rev 01A (V-301 / ST-017), 030-00 Rev 04A (V-100), 041-00 Rev 10A (V-312), 062-00 and 025-00 (the last two are Node 2 only). I rendered each page at 300 dpi to read the tags. The main tags quoted in the worksheet are on the drawings: LSHH-304 (N14), LSLL-305 (N16), LIC-302, LV-303, LG-301, PI-301C, PV-303, PSV-304A/B, BV-018, BV-019 NC, TP-01A/B to TP-04, PI-545, the check valve on 3"-PR-B013-8086-H, the LC 100 % bypass on 3"-PR-B013-8087-H, PSV-100B, LV-101B, LV-102B and LSHH/LSH/LSLL-101B. The drawing revisions in the worksheet header are correct.

The serious gaps are in the existing V-301 outlet piping just upstream of the new tie-in TP-04, which the worksheet never examines:
(a) an NC manual bypass (017) around LV-303;
(b) existing open routes from the same header to the oil heater (6"-PR-C013-152-X via FSV-010 / BV-023) and to a bullet tank (4"-PR-C013-155-X via 032-00). Drawing 041 shows that second route arriving at V-312 N5 as "FROM REPCO SEPARATOR 4"-PR-D013-155X3", bypassing ST-017;
(c) the V-301 water draw-off from N9 (valve 102) tying into the oil outlet line upstream of LV-303.

The check valve is also credited in the wrong place. TP-01A/B takes oil off the Block-1 trunkline (4"-PR-D013-103-X, 600#), upstream of the check valve on 8086-H. That check valve lets flow pass towards the strainer, so it gives no protection against trunkline pressure reaching the 150# section.

There are several citation and tag errors:
- "NC philosophy (Note 7)" is credited, but Note 7 on 030 is about free-water separation. The NC note is Note 7 on 041 and applies to V-312 nozzles.
- PCV-100B is drawn as PLV-100B.
- PI-54X has no tag number.
- Line number 3"-PR-B013-8087-H is used twice: for the strainer bypass on 031 and for a 2"-600# segment at TP-02A/B on 030.
- The 031 outlet off-page connector points to 042-00, but V-312 is on 041-00.
- The claim that the LLP header 4"-PR-D013-5076-X ends in V-312 cannot be confirmed: no such incoming line appears on 041.
- LCV-304 is outside the highlighted Node 1 path on 030, and the inspection sheet records it in good condition. Yet the worksheet uses it as a cause and puts it on the Rec 8 refurbishment list.

**Strengths noted:**

- Equipment and instrument tags on V-301 match the drawing 031 (LSHH-304 at N14, LSLL-305 at N16, LIC-302, LV-303, LG-301, PI-301C, PV-303, PSV-304A/B). The worksheet also caught that the 03-Nov inspection sheet swaps the LSHH and LSLL tags (sheet shows LSHH-305 / LSLL-304); this is in Rec 2.
- The V-301 inlet sources are listed correctly from drawing 031: BV-018 on 6"-PR-D013-153-X from the HP header, BV-019 6" NC, LAM-B/C coflex 4"-PR-D013-090-X, and the 25K LP and interim LP gas lines. Rec 4 asks for positive isolation of these.
- The worksheet spotted that ST-017 is tagged 'A/B' but drawn on 031 as a single basket with a 100 % LC bypass, and Rec 6 asks for this to be confirmed. The LC on the bypass valve on 3"-PR-B013-8087-H is quoted correctly.
- The check valve on 3"-PR-B013-8086-H (031, upstream of the 3"-150# valve where it joins 8083-H) exists as credited in deviation 3.
- The worksheet found the P&ID 030 Note 3 free-water route ('LLP HEADER [TO BULLET TANK-C]' 4"-PR-D013-5076-X) and raised it as a hazard (deviation 4, Rec 5).
- Drawing revisions in the header (031 Rev 01A, 030 Rev 04A, 041 Rev 10A) match the title blocks. The V-312 PSV is correctly not credited: no PSV is drawn on V-312 in 041, only PSD-232 / LSHH-1004 and a vent to atmosphere.
- The 150# pressure-class (spec) break at TP-04 (3"-300# valve, C013|B013) and the D013|B013 break at TP-01A/B are reflected in the worksheet's HP/LP concern (Rec 3, deviation 2 remarks).
- V-100 tags in Rec 10 (LSHH / LSH / LSLL-101B, PSV-100B, LV-101B, LV-102B) are on drawing 030 as quoted.


### A2.1 [Critical] The existing manual bypass valve (017) around LV-303 on V-301 is missing from the study. It is a direct path for gas blow-by into the 150# B013 section and V-312 that does not pass through LV-303.

- **Worksheet ref:** Dev 2 More Flow cause 1; Dev 10 Low Level cause 1; Rec 2 / Rec 3 / Rec 11
- **Evidence:** P&ID 031: 3"-PR-C013-152-X runs from N12 through (020) to valve (017), drawn filled (NC), and on to the outlet header that feeds TP-04. LV-303 sits in the parallel branch (021)-LV-303-(022). Deviations 2 and 10 only name 'LV-303 fails open / LIC-302 mis-set / LCV-304 wide open'. Deviation 1 lists (020/021/022) but never (017).
- **Recommendation:** Add a cause to deviations 2 and 10: (017) inadvertently opened or passing. Lock (017) closed, or blind it, for the trial; add it to the Rec 4 blind/lock register and the Rec 1 line-up sheet. Include the full-bore (017) case in the Rec 3 gas blow-by calculation.


### A2.2 [Critical] The existing V-301 outlet routes downstream of (017)/(022) are not studied. Trial crude can go to the oil heater or to the bullet tank through an existing line that bypasses ST-017. The worksheet treats V-301's inlets but not its other outlets.

- **Worksheet ref:** Dev 4 Mis-directed Flow (all causes); Rec 4; Dev 11 sand
- **Evidence:** P&ID 031: the outlet header past (017)/(022) continues through FSV-010 and BV-023 to 'TO OIL HEATER 6"-PR-C013-152-X (028-00)' and 'TO BULLET TANK 4"-PR-C013-155-X (032-00)'. The TP-04 tie-in tees off this same header. P&ID 041: V-312 N5 receives 'FROM REPCO SEPARATOR 4"-PR-D013-155X3 (032-00)'. This is a second V-301-to-V-312 path with no strainer. Rec 4 lists only the V-301 inlets, the V-100 outlet and the V-312 flare line.
- **Recommendation:** Add mis-directed flow causes: V-301 crude to the oil heater (028-00), and unstrained crude to V-312 or another bullet tank through 155-X. Extend Rec 4 to positively isolate BV-023 / 6"-PR-C013-152-X and 4"-PR-C013-155-X, plus the 155X3 valve at V-312 N5. Get drawing 032-00 and add it to the reference list.


### A2.3 [Major] The check valve is credited for the wrong direction and location. TP-01A/B takes oil from the Block-1 trunkline 4"-PR-D013-103-X (600#), upstream of the check valve on 8086-H. That check valve passes flow towards ST-017, so trunkline pressure reaches the 150# section with nothing in the way except the manual 3"-600# spec-break valve. Rec 3 also leaves out the trunkline as an HP source.

- **Worksheet ref:** Dev 4 cause 3 (safeguard 'Check valve - hardware'); Rec 3
- **Evidence:** P&ID 030: the purple Node 1 path drops from the 4"-PR-D013-103-X trunkline at TP-01A/01B, through a 3"-600# valve (spec break D013|B013) and DBB / PI-543, into 3"-PR-B013-8086-H. P&ID 031: the check valve on 8086-H points towards the junction with 8083-H, i.e. towards the strainer. The worksheet's consequence ('crude at trunkline pressure can back into the new 150# line if the check valve passes') has the direction backwards. Rec 3 names only well 192B CITHP and the HP header via BV-018.
- **Recommendation:** Remove the check-valve credit from deviation 4 cause 3. Add the trunkline (4"-PR-D013-103-X) and V-100 operating pressure to Rec 3 as HP sources for the B013 section. Require positive isolation at TP-01A/B whenever the V-100 route is not in use.


### A2.4 [Major] The V-301 water draw-off goes into the oil outlet line, not to a separate drain. Free water from V-301 can therefore enter the Node 1 route to V-312. The worksheet treats the draw-off only as a drainage item, and its only water safeguard is V-100 separation.

- **Worksheet ref:** Dev 11 Composition (high water cut); Dev 16 Drainage
- **Evidence:** P&ID 031: N9 / N17 has a 2" valve (102) and a 2"x1 1/2" reducer, then an arrow into 3"-PR-C013-152-X between (020) and (017), upstream of LV-303 / TP-04. No separate water level control or water outlet is drawn on V-301. Deviation 11 water-cut safeguards are 'Periodic sampling' and 'Free-water separation in V-100 (if route used)'.
- **Recommendation:** Add a cause: V-301 water draw-off (102) open or passing during transfer, sending water to V-312 and the heater (link to deviation 4 consequences). Lock (102) closed or blind it during transfers, include it in Rec 1 / Rec 4, and say how V-301 free water is to be handled.


### A2.5 [Major] Blocked outlet downstream of TP-04 is only analysed as a V-301 high-level case. Closing the ST-017 outlet valve or the V-312 inlet 3"-150# valve while LV-303 is open traps the 150# B013 section at V-301 pressure. There is no relief anywhere in the B013 section, and no thermal relief for liquid blocked in between valves.

- **Worksheet ref:** Dev 1 cause 1 (blocked outlet) and cause 2; Rec 3
- **Evidence:** P&ID 031: TP-04 3"-300# valve with C013|B013 break, 8083-H, ST-017 3"-150# inlet and outlet valves, 8085-H. P&ID 041: a further 3"-150# valve and PI-549 DBB on 8085-H at the V-312 inlet (TP-06A). No PSV or TSV is drawn on 8083 / 8085 / 8086 / 8087. The deviation 1 consequence covers only V-301 level and pressure. PI-549 and the V-312 inlet valve are not mentioned anywhere.
- **Recommendation:** Add an overpressure consequence for the B013 section to deviation 1 and cover it by name in Rec 3: blocked-in at V-301 or trunkline pressure, plus blocked-in thermal expansion between the TP-04 valve, the strainer valves and the V-312 inlet valve. List the V-312 inlet 3"-150# valve and PI-549 as Node 1 items. Note that on 041 the 8085-H segment is coloured as Node 2, so the node boundary needs stating.


### A2.6 [Major] The procedural safeguard cites the wrong note, and the drawing does not support it. There is no NC note on 031, and Note 7 on 030 says something else. The NC note is Note 7 on 041, which covers V-312 nozzles only. None of the new Node 1 valves are marked NC.

- **Worksheet ref:** Dev 3 Reverse Flow, safeguard 2 'NC valve philosophy (Note 7)'; Dev 4 cause 3 safeguard 2
- **Evidence:** P&ID 030 General Note 7: 'TEST SEPARATOR SHALL BE OPERATED FOR HOT OIL FLUSHING, IF FREE WATER SEPARATION IS REQUIRED.' P&ID 041 General Note 7: 'NC NORMALLY CLOSE IS APPLICABLE WHEN BULLET TANK IS USED FOR HOT OIL OPERATION' (NC clouds at V-312 N9 / N5 / flare). P&ID 031 has only Notes 1-3. On 030 and 031 the TP-01 / 02 / 04 valves and the 8083 / 8086 valves carry no NC marking. Only the bypass is LC.
- **Recommendation:** Correct the citation. Do not credit an 'NC philosophy' for the V-301 / V-100 routes until the P&IDs mark the valves NC / LC (Rec 1 / Rec 4). Ask Engineering to add NC / LC status to the TP-01A/B, TP-02A/B, TP-03 and TP-04 valves.


### A2.7 [Major] The free-water and V-100 routing on 030 is ambiguous, and the worksheet's reading of it cannot be confirmed from the drawings. The Node 1 purple highlight on 030 runs continuously from TP-02A/B (the 2" line downstream of the LV-102B water valve, marked NOTE-3) through TP-03 and TP-01A/B into 8086-H to the strainer. The worksheet's statement that 4"-PR-D013-5076-X 'terminates in V-312' cannot be checked: no incoming 5076-X appears on 041.

- **Worksheet ref:** Dev 4 cause 1; Rec 5; Dev 11 cause 2
- **Evidence:** P&ID 030: purple path TP-02A/02B -> 2"-600# valve -> 2"-600# check valve -> TP-03 -> vertical 4" -> TP-01A/01B -> 3"-600# -> 3"-PR-B013-8086-H. 'LLP HEADER [TO BULLET TANK-C] 4"-PR-D013-5076-X -> M0001-041-00'. P&ID 041 shows only 'FROM NEW LLP HEADER 10"-PR-D013-3010-H (004-00)'. There is no 5076-X off-page connector.
- **Recommendation:** Before closing Rec 5, have Engineering mark up which V-100 outlet (oil via LV-101B or water via LV-102B) actually feeds ST-017, and where 5076-X ends on 041 or 004. Fix the Node 1 highlight on 030 if the water line is not part of the oil route. Restate deviation 4 cause 1 and deviation 11 cause 2 once this is known.


### A2.8 [Major] HP/LP interfaces shown on the drawings are not listed in the design basis or in Rec 3. V-301 is fed from 600# (D013) sources through a D013|C013 spec break, and its outlet is 300# (C013) up to TP-04. P&ID 030 Note 5 says V-100 runs close to the wellhead choke downstream pressure. Rec 3 considers only well 192B CITHP and BV-018.

- **Worksheet ref:** Header Design Conditions; Rec 3; Dev 5
- **Evidence:** P&ID 031: C013|D013 spec breaks at N20 and at (008) / BV-018; C013|B013 at TP-04. P&ID 030 Note 5: 'TEST SEPARATOR SHALL BE OPERATED CLOSE TO THE WELLHEAD CHOKE VALVE DOWNSTREAM PRESSURE'. Worksheet header: 'DP = V-100 55 barg | V-301 TBC'.
- **Recommendation:** Widen Rec 3 to cover V-301 and C013 rating against the D013 inlet sources, V-100 at choke-downstream pressure through TP-01A/B, and the trunkline. State in the header which pressure-class (spec) break each source crosses.


### A2.9 [Major] PSV-304A is credited without checking its inlet and outlet block valves, which are not shown locked or car-sealed open. The open nozzle left by the removed PSV-304B is also not addressed.

- **Worksheet ref:** Dev 1 cause 2 / Dev 5 / Dev 13 safeguard 'PSV-304A - vessel only'; Rec 9
- **Evidence:** P&ID 031: PSV-304A has 2" inlet (013) and 3" outlet (014) block valves; PSV-304B has 2" inlet (015) and 3" outlet (016). Neither pair carries a CSO / LO mark. The inspection sheet says PSV-304B is 'missing in field (sent for yearly calibration)'.
- **Recommendation:** Credit PSV-304A only once (013) and (014) are verified car-sealed or locked open. Confirm that (015) and (016) are closed with blind flanges on the open nozzles while PSV-304B is away. Add this to Rec 9 and the PSSR.


### A2.10 [Major] Drawing 041 shows other HP and unfiltered sources piped into V-312, the receiving tank of Node 1, including a direct wellhead line. The worksheet does not mention them. They overlap with Node 2, but they bear on whether V-312 is dedicated and on the HP/LP basis.

- **Worksheet ref:** Not addressed (V-312 inlets); Dev 4
- **Evidence:** P&ID 041 at N5: 'FROM WH 193 CHP 3"-PR-D013-WH193X2-X' through 3",600# BV-XXX, 'FROM REPCO SEPARATOR 4"-PR-D013-155X3', and 'TO INTERIM LP BULLET TANK 3"-PR-D013-4120-X'. These connect at N5 through BV-XXX (3",600#, marked NC), whose valve tag is unassigned. Note 4 says the bullet tank is dedicated, but isolation is by NC manual valves only.
- **Recommendation:** Either record these in Node 1 deviation 4 (mis-directed flow) or confirm they are carried in Node 2. Require positive isolation of the WH193 and 155X3 inlets in the Rec 4 blind register while V-312 is on atmospheric vent.


### A2.11 [Minor] PI-54X is a placeholder tag. There is no dP instrument, only two separate local PIs. PI-545 sits on 8083-H upstream of the TP-04 junction, so it measures LP-section pressure, not V-301 pressure as Rec 11 implies.

- **Worksheet ref:** Dev 1 cause 3 safeguard 1 'PI-545 / PI-54X local dP'; Rec 11
- **Evidence:** P&ID 031: 'PI 545' with DBB on 3"-PR-B013-8083-H, and 'PI 54X' downstream of ST-017. Other new PIs are PI-543 / PI-544 (030) and PI-549 (041). Rec 11: 'PI-545 read every 10 min against a stop limit'.
- **Recommendation:** Get the PI-54X tag number assigned. Write the safeguard as 'two local PIs (PI-545 upstream / PI-54X downstream)'. Make clear that Rec 11 uses PI-545 as LP-section pressure and PI-301C for V-301 pressure.


### A2.12 [Minor] Line number 3"-PR-B013-8087-H is used for two different lines, and on 030 the size and class do not match the line.

- **Worksheet ref:** Line numbers (Rec 6 / Dev 1 cause 3)
- **Evidence:** P&ID 031: 3"-PR-B013-8087-H is the ST-017 100 % bypass. P&ID 030: the label '3"-PR-B013-8087-H' sits on the new 2"-600# segment at TP-02A/B (NOTE-3), next to 2"-600# valves and a check valve.
- **Recommendation:** Raise a P&ID comment to give the 030 segment its own line number with the correct size and class (2", D-class), and correct any worksheet references once that is done.


### A2.13 [Minor] Off-page connectors do not match, and some referenced drawings are missing from the study basis.

- **Worksheet ref:** Header drawing list
- **Evidence:** P&ID 031 outlet connector reads 'TO BULLET TANK-C INLET [L028-21-V-312] L028-PR-PID-01-M0001-042-00', but V-312 is on 041-00 (and 041 refers back to 031-00). Drawing 032-00 (LAM-16 flare, existing bullet tank route 155-X, HP header, coflex) and 028-00 (oil heater) are referenced on 031 but not listed in the worksheet basis.
- **Recommendation:** Correct the off-page connector from 042-00 to 041-00. Add 032-00 and 028-00 to the HAZOP reference drawings, or record why they are outside the node.


### A2.14 [Minor] Some V-100 tags do not match the P&ID or inspection sheet, and LCV-304 does not appear to be in the highlighted Node 1 path.

- **Worksheet ref:** Dev 1 cause 4; Dev 2 cause 1; Dev 13; Rec 8; Dev 18
- **Evidence:** P&ID 030: the V-100 gas pressure valve is tagged PLV-100B; the worksheet says PCV-100B (the inspection sheet uses PCV-100B). LCV-304 is on 2"-PR-D013-3406-H at the bottom of 030, outside the purple Node 1 highlight; the V-100 oil level valve on the outlet is LV-101B with FIT-102C. The inspection sheet records L028-21-LCV-304 as 'good physical condition', yet Rec 8 lists it for refurbishment. LC-101B (inspection sheet) is not visible on 030, where an unnumbered 'LLC' is shown.
- **Recommendation:** Line up tags with the P&ID (PLV-100B). Confirm what LCV-304 does and whether it is in Node 1, and remove it from Rec 8 if it is not needed. Get LC-101B tagged on the P&ID.


### A2.15 [Observation] The statement 'no tracing / insulation shown' may conflict with the line designations. All new Node 1 lines end in '-H' (8083/8085/8086/8087-H), while existing lines end in '-X' or '-E40', which suggests an insulation or tracing code is assigned. The legend sheets (STDS-PR-PID-1-0001-01 to -05) were not provided, so this cannot be confirmed.

- **Worksheet ref:** Dev 8 Low Temperature cause 1
- **Evidence:** P&ID 031 / 030 line numbers ending in '-H'. P&ID 030 shows separate 'INSULATION / NO INSULATION' break markers on existing lines.
- **Recommendation:** Check the insulation code '-H' against the legend sheets and the line list. Update the deviation 8 cause and safeguard wording to match.


### A2.16 [Observation] The existing NC bypass (016) around PV-303 on the V-301 gas outlet is not mentioned. Opening it during a PV-303 failure, or leaving it open, changes V-301 pressure, and it is a likely operator workaround while PV-303 is corroded.

- **Worksheet ref:** Dev 5 cause 1 / Dev 13
- **Evidence:** P&ID 031: 6"-PR-C013-148-X loop with a 4" valve (016) drawn filled (NC) around BV-011 / PV-303 / BV-012.
- **Recommendation:** Mention (016) in deviations 5 and 6, and state its required position in the Rec 1 line-up.


## A3. Safeguard validity vs field condition

**Reviewer summary.** Safeguard validity vs field condition review of Node 1 (V-301 / V-100 to V-312 via ST-017). The worksheet sets the right policy: anything non-functional or untested gets no credit. It applies that policy correctly to the headline V-301 items: LSHH-304 and LSLL-305 (whose transposition on the inspection sheet is confirmed by P&ID 031), LCP L028-82-LCP-002 and LSHH-101B. It does not apply the policy consistently in the rest of the worksheet. Problems found: (a) the 'Effective Safeguards' column still lists items that are defective, undefined, missing or not specific to the consequence. These are the V-312 PSV (no PSV is visible on P&ID 041), the corroded V-100 level gauge, an integrity inspection programme that has already been shown not to work, a 'locked closed' strainer bypass that the cause itself defeats, and vessel-only PSVs credited against downstream gas blow-by. (b) A check valve is credited against trunkline back-flow, but on P&IDs 030/031 it sits in the forward direction for that path. (c) Several current-risk likelihoods are lower than equivalent rows with the same or fewer barriers (row 1.4 L3 vs row 1.2 L4; row 13 L3 vs rows 2/10 L4; row 18 L3 despite observed severe corrosion), which suggests implicit credit. (d) Residual risk for the principal gas blow-by scenario (C4 to C2) is taken before the Rec 14 LOPA. It depends on reinstating an LSLL whose final element is unknown and need not be independent of LV-303. Rec 2 also allows the alternative 'no shutdown function exists', which would cancel that reduction. (e) Operator response (Rec 11, 5 min) is set without a process safety time and relies on local gauges and a remote well choke. (f) The hot oil unit condition report was left out of the Node 1 basis. It is relevant: Node 1 sends sand, water and possible gas blow-by to V-312, the HOU heater and the engine. That report shows the heater low-flow and high-temperature switches defective, the ESD button inoperable, and the engine emergency air shut-off failing to respond to ESD. Meanwhile row 15 says Node 1 has 'no new ignition source', and Node 2 is blank. The trial should not proceed until Recs 2, 3 and 9 are closed as hold points, the V-312 relief basis is shown to exist, and the HOU protections are restored or explicitly not credited in Node 2.

**Strengths noted:**

- States the credit rule in the header ('non-functional / untested items not credited') and applies it to the V-301 LSHH/LSLL, LCP L028-82-LCP-002 and V-100 LSHH-101B (rows 1.2, 1.4, 2, 9, 10, 19).
- Correctly found that the Repco inspection sheet tags are transposed (sheet: LSHH-305 / LSLL-304). P&ID 031 shows LSHH-304 on N14/N13 and LSLL-305 on N16/N15, which matches the worksheet.
- Picked out HP/LP interface gas blow-by (3"-B013 150# line, ST-017, V-312 DP 20 barg) as the principal scenario. It rejects the draft 'overpressure not credible' statement and asks for an API 521 calculation (Rec 3) and a LOPA (Rec 14).
- Rec 11 makes credit for 'local gauge + operator' conditional on a dedicated operator, painted marks, written stop actions and a defined response time. This is the right approach for procedural safeguards.
- Rec 10 excludes the V-100 route unless its level switches are tested and LV-102B / PCV-100B / IA manifold are refurbished. This matches the TDE inspection findings.
- Treats valve fail positions as not verified (Rec 8, row 13) and recognises that the corroded V-100 IA manifold makes loss of instrument air credible.
- Row 18 recognises the corroded PV-303 / LV-102B / PCV-100B bodies as a pre-existing LOPC risk that exists independently of the trial.
- Rec 9 picks up PSV-304B being off-site and requires either reinstatement or a sizing demonstration for PSV-304A alone.
- Row 1.3 / Rec 6 recognises that the 100% strainer bypass is a credible operator action and an unfiltered-sand path to the heater.


### A3.1 [Critical] A V-312 PSV is listed as a safeguard for gas blow-by, but no PSV for V-312 can be seen on the P&IDs. With LSLL-305 not credited, the principal overpressure scenario has no hardware barrier at all.

- **Worksheet ref:** Row 2 (More Flow) safeguard 2; Rows 10 and 13; Rec 3
- **Evidence:** Row 2 Effective Safeguards: '2. V-312 PSV: tag / set / discharge NOT CONFIRMED.' P&ID 041 (page 3) shows on V-312 only LSHH-1004 / LSLL-1004 with PSD-232 / PSD-231 and LT/LG-1004; no PSV tag is visible, and the text layer also has no PSV on V-312. Note 5 on P&ID 041: the vent to atmosphere is operated by closing the line to the LAM-16 flare, so during stabilisation the only open relief path is 2"-VF-B013-8095-X to the atmospheric vent (dispersion calculation still on HOLD 1). The source side is unknown: V-301 DP is 'TBC', well 192B CITHP is 'INPUT REQUIRED', and 150# B013 is rated 19.6 barg at 38 C.
- **Recommendation:** Remove the V-312 PSV from the Effective Safeguards column. Record explicitly that rows 2, 10 and 13 currently have NO hardware barrier. Rewrite Rec 3 as a mandatory hold point before the first batch: confirm whether a V-312 PSV exists (tag, set, capacity for the gas blow-by rate through LV-303 / LCV-304 at maximum source pressure, discharge location). If none exists, provide a PSV or an independent, tested LSLL/PSHH trip on a dedicated final element before introducing any hydrocarbon.


### A3.2 [Major] The hot oil unit condition report is left out of the condition basis and is not handled anywhere, although Node 1 consequences end up in the HOU. The report also shows that the HOU ignition-source isolation (ESD, engine emergency air shut-off) and the heater protections have failed.

- **Worksheet ref:** Header (equipment condition basis); Rows 1.3, 4.1, 11.1, 11.2, 15; Rec 6; Node 2 (blank)
- **Evidence:** Header: 'Equipment condition basis: Repco / TDE inspection sheets 03-Nov-2026' (HOU report not cited). HOU report: Murphy low-pressure switch and high-temperature switch 'fails to respond... static, ideal value'; heater low-flow indication switch and flame reset 'mechanical damage'; alarm bypass switch non-functional; burner ESD button 'completely damaged and inoperable'; 'emergency air shut-off valve failed to respond to the ESD signal' (burner LCP and engine LCP item 18); burner LCP internals 'extensive corrosion'. Node 1 rows 1.3 / 11.1 rate sand to the heater coil as 'hot spots, coil failure, fire / explosion' (People C). Row 4.1 rates water causing 'steam flash in the heater coil'. Row 15 says 'no new ignition source in Node 1'. Rows 2 / 10 give gas blow-by to the atmospheric V-312 vent with 'fire / explosion'. The worksheet Node 2 table is empty.
- **Recommendation:** Add the HOU condition report to the study basis. In Node 1 rows 1.3, 4.1, 11.1 and 2/10, record that no heater low-flow, high-temperature or ESD protection can be credited downstream, and that the fired heater and the HOU engine are ignition sources for a gas blow-by cloud from the V-312 vent. Before any batch: repair and function-test the burner/engine ESD and the emergency air shut-off valve, and replace the low-flow, high-temperature and low-pressure switches. Complete Node 2 with these items as NOT CREDITED until tested. Change the Rec 6 statement 'bypass not to be used with the heater lit' from procedure-only to a verifiable control.


### A3.3 [Major] Residual risk for the gas blow-by scenario drops two likelihood steps before the LOPA (Rec 14) has been done. It depends on reinstating LSLL-305, whose final element is unknown and is not required to be independent of the initiating cause (LV-303 / LIC-302 failing open). Rec 2 also offers the alternative 'record formally that no shutdown function exists', which would cancel the residual credit.

- **Worksheet ref:** Rows 2 and 10 residual risk (People C2 RR3); Rec 2; Rec 14
- **Evidence:** Rec 2: '...identify and implement their final element from the Repco C&E, commission LCP L028-82-LCP-002 or record formally that no shutdown function exists'. The Repco inspection sheet says the LCP 'has never been put into active service'; push buttons are rusted and non-functioning and the status lamps are entirely non-functional. Rows 2/10: current C4 RR2 becomes residual C2 RR3. Rec 14: 'LOPA for the gas blow-by scenario... once Recs 2 and 3 define the available protection'.
- **Recommendation:** Mark the residual rows 2/10/13 'TBD pending LOPA (Rec 14)' instead of C2. In Rec 2, require the LSLL-305 trip to act on a final element independent of LV-303 (for example a dedicated SDV on the 3" oil outlet or closure of the well 192B inlet), with a logic solver independent of LIC-302, a documented proof test, and a PFD consistent with the LOPA target. Delete the 'no shutdown function exists' option, or state that if it is chosen the trial cannot proceed without an alternative IPL.


### A3.4 [Major] The check valve credited against trunkline crude backing into the new 150# line appears, on the P&IDs, to be oriented forward for that flow path. It is not an effective or specific safeguard for this cause.

- **Worksheet ref:** Row 4 cause 3 (V-100 outlet to trunklines) safeguard 1 'Check valve - hardware'
- **Evidence:** P&ID 030 (page 2): the trunkline branches 4"-PR-D013-103-X (Block-1 8" trunkline) and 4"-PR-D013-120-X (LAM-A export) leave the V-100 oil outlet upstream of TP-01A/B and 3"-PR-B013-8086-H. P&ID 031 (page 1): the check valve on 3"-PR-B013-8086-H points towards ST-017 / V-312. Trunkline back-flow would therefore pass forward through it into the 150# section. The check valve only protects against V-301 back-flow into the V-100 line (row 3). The trunkline operating pressure is not stated. The reading is from the marked-up drawings; any check valves on the existing trunkline branches could not be confirmed.
- **Recommendation:** Remove the check valve as a safeguard for row 4 cause 3. Re-rank it using the trunkline pressure against the 150# rating; this may become a People C / overpressure scenario. Rely on Rec 4 positive isolation (spectacle blind on the V-100 outlet to the trunklines) as a pre-start hold point verified in the blind register, and add trunkline maximum pressure to the Rec 3 calculation.


### A3.5 [Major] Vessel PSVs are credited for a consequence they do not protect against, and the current likelihood is one step lower than in rows 2/10, which have the same consequence. This implies credit for a safeguard that is not specific to the consequence.

- **Worksheet ref:** Row 13 (Loss of Utilities) safeguards and current likelihood L3; compare Rows 2 / 10 (L4)
- **Evidence:** Row 13 consequence: 'Fail-open LV: gas blow-by (deviation 10)'. Safeguard: '1. PSV-304A / PSV-100B - vessels only.' Current People C3 RR3, while rows 2 and 10 (same gas blow-by) are C4 RR2. PSV-304A and PSV-100B protect V-301 and V-100, not the downstream 3"-B013 150# line, ST-017 or V-312. Loss of instrument air is made more likely by the 'severe corrosion' of the V-100 instrument air manifold (TDE sheet item 8).
- **Recommendation:** Rank the row 13 gas blow-by branch consistently with rows 2/10 (C4 RR2) or split row 13 into separate cause/consequence pairs. Credit PSV-304A / PSV-100B only for vessel overpressure. Also analyse the common-cause case where one instrument air loss makes LV-303 fail open and PV-303 fail closed at the same time (blow-by at elevated V-301 pressure); fail positions are not verified (Rec 8).


### A3.6 [Major] A corroded level gauge is credited as a procedural safeguard. The V-100 route is ranked one likelihood step lower than the V-301 route even though it has fewer functional barriers. Rec 10's 'function-test LSHH / LSH / LSLL-101B' cannot give a trip because V-100 has no LCP or logic solver.

- **Worksheet ref:** Row 1 cause 4 (V-100 LV fail closed): safeguard 3 and current L3; Rec 10
- **Evidence:** Row 1.4 safeguards: '3. Level gauge (corroded) - procedural'. TDE sheet item 11: 'The level gauge and associated nuts and bolts are corroded'. TDE item 1: 'No local control panel (LCP) is installed for test separator L028-21-V-100'. Item 3: LV-102B 'Severe corrosion... body and stem'. Item 8: instrument air manifold severe corrosion. Row 1.4 current People D3 vs row 1.2 (V-301, functional LG-301 per Repco item 9) D4.
- **Recommendation:** Do not credit the V-100 level gauge until its integrity and readability are confirmed. Rank row 1.4 at L4 or higher, consistent with row 1.2. The corroded gauge-glass bolting is itself an LOPC source; add it to row 18. Reword Rec 10: the V-100 route may be used only after a logic solver and final element are provided and proof-tested for the 101B/102B switches, not just after the switches are 'inspected and function-tested'.


### A3.7 [Major] Operator response is made creditable (5 min) without a process safety time and relies only on local indication. For gas blow-by, a PI read every 10 minutes cannot detect the event in time, and 'close well 192B choke at high mark' is a remote action.

- **Worksheet ref:** Rows 1.2, 2, 9, 10, 12 - Rec 11 (manning / operator response)
- **Evidence:** Rec 11: '...PI-545 read every 10 min against a stop limit... response time to any deviation not more than 5 min, otherwise "local gauge + operator" is not credited.' Rows 2/10 list 'PI-545 local - procedural' as a safeguard against gas blow-by. P&ID 031: PI-545 is a local gauge at TP-04 upstream of ST-017. No alarm, no CCR indication and no V-301 LCP in service (Repco sheet item 1). Row 1.2 notes V-301 is 'not continuously manned'. The time from the high mark to carry-over, or from the low mark to blow-by, is not calculated anywhere.
- **Recommendation:** Calculate the process safety time for V-301 high level (mark to N1 gas outlet) and low level (mark to LV-303 uncovering) at the maximum well 192B rate. Credit the operator only if detection plus decision plus action (including radio and choke closure travel time) is well within it. Do not list PI-545 as a safeguard for gas blow-by. A local PI can at most confirm that a deviation is happening, not prevent it.


### A3.8 [Major] The safeguard is defeated by its own cause, and two safeguards in different rows contradict each other: 'bypass locked closed' versus 'bypass allows isolation'.

- **Worksheet ref:** Row 1 cause 3 (strainer blockage) safeguard 2; Row 17 safeguard 2
- **Evidence:** Row 1.3 cause: '...operator opens the 100 % bypass (LC) to maintain flow'. Safeguard: '2. Bypass locked closed - procedural.' Row 17 safeguard: '2. Bypass allows isolation - hardware.' P&ID 031 shows a single ST-017 body with an 'LC' 3"-150# valve on the '100% BYPASS', although the title is 'ST-017 A/B'. The cause also says ST-017 has 'local PIs only, no dP alarm'. PI-54X downstream of the strainer has no assigned tag number, so it is not yet a defined or commissioned instrument.
- **Recommendation:** Remove 'bypass locked closed' as a safeguard for row 1.3; the cause is that the lock is overridden. Remove 'bypass allows isolation' from row 17, because using the bypass reinstates the row 1.3 unfiltered-sand consequence. Credit neither until Rec 6 is closed (key-controlled LC under PTW, or a true A/B duty/standby arrangement). Assign a real tag for PI-54X.


### A3.9 [Major] PSV-304A is the only remaining relief device on V-301, but its credit cannot be audited. No set pressure, V-301 DP, relief case capacity or test record is available. The status of the PSV-304B isolation valves while it is off-site is not recorded.

- **Worksheet ref:** Rows 1.2, 4.2, 5.1, 13 - PSV-304A credited; Rec 9
- **Evidence:** Repco sheet item 8: 'PSV L028-21-PSV-304A available but L-028-21-PSV-304B is missing in field (sent for yearly calibration)'. No condition, test date or set pressure is given for 304A. Header: V-301 DP 'TBC (INPUT)'. P&ID 031 shows PSV-304B with inlet and outlet block valves (015) / (016) and PSV-304A with (014) / (013). Row 4.2 credits PSV-304A for HP header inflow through 6" BV-018 without a sizing check.
- **Recommendation:** Make Rec 9 a pre-start hold point. Before any credit, obtain PSV-304A's set pressure and last test certificate and confirm they match the V-301 MAWP. Show that 304A alone covers blocked outlet, the HP-header inflow through BV-018, and control valve failure. Confirm that the PSV-304B inlet (015) is locked closed and the open flanges are blinded while the valve is away, and that the 304A inlet/outlet valves are car-sealed open. Record this in the blind/CSO register.


### A3.10 [Major] An integrity inspection programme is credited even though the 03-Nov inspections show it has not prevented severe corrosion. The likelihood (L3) understates a degraded condition that already exists.

- **Worksheet ref:** Row 18 (Corrosion / Erosion) safeguard 'Integrity inspection programme' and current People D3
- **Evidence:** Row 18 cause: 'existing severe corrosion on valve bodies and stems'. Safeguard: '1. Integrity inspection programme - procedural.' Evidence: Repco item 6 (PV-303 severe corrosion, body and stem), TDE item 3 (LV-102B), item 6 (PCV-100B), item 8 (IA manifold), item 11 (level gauge bolting). Row 18 current People D3, residual D2.
- **Recommendation:** Remove the inspection programme as a credited safeguard, or record it as demonstrably ineffective. Re-rank the current likelihood at L4 or higher. Require refurbishment or replacement of PV-303, LV-102B and PCV-100B before they see trial service. Rec 8 says 'validate under live conditions' and row 17 lists 'refurbishment... under live conditions'. Separate these: refurbishment must be done positively isolated, and only the functional validation done live.


### A3.11 [Minor] On P&ID 031, LG-301 and the LIC-302 displacer appear to share the same bridle and nozzle isolation. A plugged bridle (waxy, sandy crude is the cause in rows 8 and 11) would disable both the control loop (a cause) and the operator's only level indication (a safeguard). That is a common-cause failure.

- **Worksheet ref:** Rows 1.2, 9 - LG-301 / LIC-302 credited as indication and control
- **Evidence:** P&ID 031 (page 1): LIC-302 and LG-301 are drawn on one standpipe and bridle on the V-301 east side with shared 1" / 1/2" valves; LSHH-304 and LSLL-305 have separate nozzles N14/N13 and N16/N15. Rows 8 and 11 identify wax and sand. This is a reading of a marked-up drawing; confirm in the field.
- **Recommendation:** Verify the bridle arrangement in the field. If LG-301 and LIC-302 share it, do not credit LG-301 as independent of the LIC-302 failure causes. Add bridle blow-down before each batch to the SOP (Rec 1) and rely on LSHH-304 / LSLL-305 on their own nozzles for independence.


### A3.12 [Minor] The 'Effective Safeguards' column mixes credited barriers with items that are explicitly not credited, undefined, or design notes. It is hard to audit what was credited in each L value.

- **Worksheet ref:** Effective Safeguards column generally (Rows 1.2, 2, 9, 10, 11.1, 11.2, 14)
- **Evidence:** For example row 1.2 '3. LSHH-304 / LCP: NOT CREDITED'. Row 2 '1. LSLL-305: NOT CREDITED' and 'V-312 PSV: NOT CONFIRMED'. Row 11.1 'Periodic sampling... (frequency and limits not defined)' and 'ST-017... (new; 100 % bypass LC)' (P&ID 031 Note 3: 'Basket strainer is available in stock', i.e. not yet installed). Row 14 'Existing sample points' while the cause says 'no sample point shown'.
- **Recommendation:** Split the column into 'Credited safeguards (with basis)' and 'Existing but not credited (reason)'. For each credited item state the type (IPL / non-IPL), test evidence and, for procedural items, the response time. Do not credit new equipment (ST-017, PI-54X, check valve) until it is installed, inspected and part of the PSSR.


### A3.13 [Minor] Some recommendation and cause items do not match the inspection sheets. One inspected control valve is not mentioned at all, and the V-301 instrument air supply was never inspected but is assumed.

- **Worksheet ref:** Rec 8; Row 1.4 cause; Row 13 cause
- **Evidence:** TDE item 2: 'L028-21-LCV-304... good physical condition', yet Rec 8 lists LCV-304 under 'Refurbish'. TDE item 3 second line: an LCV 'No proper tag. Mentioned tag is 910091-010', in good condition and needing paint; it does not appear anywhere in the worksheet. The Repco sheet does not cover the V-301 instrument air supply, but row 13 treats instrument air loss on LV-303 / PV-303 the same way as for V-100.
- **Recommendation:** Reword Rec 8 to separate 'refurbish' (LV-303, PV-303, LV-102B, PCV-100B, IA manifold) from 'validate / replace gauges' (LCV-304, LC-101B, Fisher PIC / LIC). Add a tag reconciliation action for valve 910091-010 and confirm its service. Add inspection of the V-301 instrument air supply and filter regulators.


### A3.14 [Minor] Fire and gas detection and executive action are not considered anywhere in Node 1. Their status is unknown, and the LCP lamps suggest an F&G shutdown function that has never been in service.

- **Worksheet ref:** Rows 2, 10, 12, 15 - fire/explosion consequences
- **Evidence:** Repco sheet item 1: indication lamps 'Local Shutdown, Remote Shutdown, F&G Shutdown' are 'entirely non-functional' and the LCP was 'never been put into active service'. Rows 2/10 list 'fire / explosion' and row 12 'LOPC at new flanges and DBB bleeds', but no gas detection is listed or assessed.
- **Recommendation:** Record F&G coverage of V-301, ST-017, the new 3"-B013 lines and the V-312 vent area, its condition and test status, and its executive actions (including tripping the HOU burner and engine). Mark it NOT CREDITED until it is verified. Add an action to confirm the F&G shutdown wiring to LCP L028-82-LCP-002.


### A3.15 [Minor] Normally-closed manual valves are credited as procedural safeguards without locking or car-seal control. The note cited applies to a different drawing.

- **Worksheet ref:** Rows 3, 4.3 - 'NC valve philosophy (Note 7)'
- **Evidence:** Row 3: 'NC valve philosophy (Note 7) - procedural'. Note 7 on P&ID 041 reads 'NC normally close is applicable when bullet tank is used for hot oil operation'. Note 7 on P&ID 030 concerns operating V-100 for free-water separation. P&ID 031 shows BV-019 as '6" NC' with no LC/CSC marking.
- **Recommendation:** Cite the correct drawing and note. Convert the NC valves on cross-connections into locked-closed or car-seal-closed valves recorded in the CSO/LC register, or rely on the Rec 4 blinds. Do not credit an NC position alone.


### A3.16 [Observation] The condition evidence cannot be fully verified. The HOU report is incomplete (broken numbering, no date). The 03-Nov-2026 date of the Repco and TDE sheets cited in the worksheet header does not appear in the extracted sheet text.

- **Worksheet ref:** Header (condition basis date); HOU condition report
- **Evidence:** HOU report S.No column contains '#REF!' twice and jumps 1, 2, #REF!, 6, 7, 15-20 (items 3-5 and 8-14 missing). Neither the HOU report nor the extracted inspection sheet text carries an inspection date or inspector signature.
- **Recommendation:** Get a complete, dated and signed condition survey for the HOU and both separators, with function-test records, and reference it by document number in the HAZOP basis. Treat any equipment not covered by the survey as untested and therefore not credited.


## A4. Overpressure, relief & engineering basis

**Reviewer summary.** Lens: overpressure, relief and engineering basis. The Node 1 worksheet is better than most. It refuses credit for the dead V-301 trips, says plainly that "overpressure not credible" is wrong, and raises Rec 3, an HP/LP interface calculation per API 521 that must be done before the trial. The problem is that the study is marked "completed" while the pressure basis it depends on is still open. Well 192B CITHP, the V-301 design pressure and PSV set pressure, the ST-017 rating, whether V-312 has a PSV and where it discharges, the H2S content, the cold-vent dispersion study (HOLD 1 on drawings 041 and 025) and the flushing-mode node (Node 3, "to be added") are all unknown. Every current and residual ranking for the gas blow-by and overpressure deviations (2, 5, 10, 13) rests on these unknowns. Node 1 should be recorded as open with formal hold points, not closed.

The study also misses or understates several items:
- **Blocked-in liquid overpressure.** The 150# section can be overpressured by liquid alone when its downstream end is closed, with no blow-by needed.
- **Unprotected spec breaks.** The breaks C013/B013 at TP-04 (drawing 031) and D013/B013 at TP-01A/B (drawing 030) have no relief device on the low-pressure side.
- **V-312 relief.** No PSV is visible on V-312, and Rec 4 would blind its flare line, leaving the 2" cold vent as the only relief path.
- **V-100 route.** V-100 is designed for 55 barg and run near wellhead pressure, yet it is left out of Rec 3.
- **Check valve as protection.** A single check valve is credited against trunkline pressure.
- **Second V-301 to V-312 path.** The existing line 155 from V-301 to V-312 is not in the worksheet or Rec 4.
- **Fire and thermal relief.** Neither case is assessed.
- **Rating mismatch.** The new lines are rated below V-312's 20 barg design pressure.
- **Shared vent.** The new vent is shared with V-001 and the open drain tank.
- **Process effects.** Sour-service materials, flashing two-phase flow, Joule-Thomson cooling, hot oil from flushing mode, reverse flow from V-312, and static in an air-ingressed V-312 are not addressed.

The trial should not start until Rec 3 is extended to cover these cases and its results are back in the worksheet.

**Strengths noted:**

- The design-basis line spells out the 150# rating with temperature derating (19.6 barg at 38 °C, 17.7 barg at 93 °C) and lists each element's design pressure, leaving 'TBC' where values are unknown instead of guessing.
- Safeguards are ranked as found in the 03-Nov-2026 inspection: LSHH-304/LSLL-305, LCP L028-82-LCP-002 and PV-303 are explicitly NOT CREDITED, in line with the chairman's 27-Oct instruction.
- It correctly rejects the draft statement 'overpressure not credible'. The remark on Dev 2 points out that it covered V-301 only and that the 150# line, ST-017 and V-312 are the exposed items.
- Rec 3 asks for a calculation per API 521 covering CITHP and the HP header via BV-018 against the line, ST-017 and V-312 ratings, and requires a PSV or independent trip before the trial if any element cannot withstand the source pressure. That is the right control.
- Gas blow-by on loss of V-301 level is named as the principal overpressure scenario (Dev 2 and Dev 10), with LOPA required (Rec 14).
- It catches the transposed LSHH/LSLL tags between the inspection sheet and the P&ID (P&ID 031 shows LSHH-304 and LSLL-305), the missing PSV-304B (Rec 9), and the free-water drain from V-100 into V-312 (Rec 5, P&ID 030 Note 3).
- Positive isolation of the HP header and coflex inlets to V-301 (BV-018/BV-019) by spectacle blind (Rec 4) recognises that manually closed valves are not an adequate HP/LP barrier.


### A4.1 [Critical] Node 1 is issued as 'completed' while the pressure and relief basis is undefined, so the overpressure scenarios cannot be ranked and these should have been formal hold points. The open items are: well 192B CITHP; V-301 operating and design pressure; the V-301 PSV set pressure (not stated anywhere); the ST-017 rating; whether V-312 has a PSV, and its set pressure and discharge; the H2S content; the cold-vent dispersion study (HOLD 1); and the flushing-mode node. The residual rankings for Dev 2 and Dev 10 (People C2, RR3) assume Rec 3 will show the system is acceptable, which is not known.

- **Worksheet ref:** Design Conditions header; Dev 19 (Any Other Safety Issue) remark; Dev 2, 5, 10, 13 rankings; Dev 7 remark (Node 3 'to be added')
- **Evidence:** Header: 'OP = V-301 operating pressure TBC (max = well 192B CITHP - INPUT REQUIRED)', 'V-301 TBC (INPUT)', 'ST-017 TBC'. Dev 19 remark: 'Inputs still required: well 192B CITHP, V-301 design data, MOC number.' Dev 2 safeguard: 'V-312 PSV: tag / set / discharge NOT CONFIRMED'. P&ID 041 and 025 both carry 'HOLD 1. New cold vent stack height based on dispersion calculation'. Dev 7: 'to be studied in Node 3 (to be added)'. Document title: '...Node_1_completed-10_Nov_2026'.
- **Recommendation:** Re-issue Node 1 as 'open with hold points'. List each TBC item as a numbered hold point with an owner, and record that no batch may start until Rec 3, Rec 9, Rec 14, HOLD 1 and the Node 3 review are closed and the worksheet has been re-convened to confirm the rankings. Mark the residual risks for Dev 2, 5, 10 and 13 'TBD pending Rec 3/14' instead of assigning C2/RR3.


### A4.2 [Critical] The 150# section can be overpressured by blocked-in liquid, with no blow-by needed, and the worksheet does not see it. The V-301 liquid line upstream is class C013 and the V-100 line is class D013 (by class code most likely 300# and 600#; not confirmed against the piping class index). The spec breaks at TP-04 (C013/B013, just downstream of valve (022), flange shown '3"-300#') and at TP-01A/B (D013/B013, at a '3"-600#' valve) have no relief device on the 150# side. If ST-017's outlet or the V-312 inlet valves (3"-150#, BV-352) are shut while (022) or the V-100 outlet is open, the whole 3"-B013 line and ST-017 settle out at separator pressure plus static head. Dev 1 only records the consequence as V-301 level rise and carry-over to the flare.

- **Worksheet ref:** Dev 1 (No/Less Flow) cause 1 and consequence 1; Rec 3
- **Evidence:** P&ID 031: 'C013 | B013' break at TP-04 after valve (022), '3"-300#'. New lines 3"-PR-B013-8083/8085/8087-H, all flanges '3"-150#'. P&ID 030: 'D013 B013' break at TP-01A/B with a '3"-600#' valve and DBB PI-543. P&ID 030 Note 5: 'Test separator shall be operated close to the wellhead choke valve downstream pressure.' Dev 1 cause 1 lists the 'strainer inlet / outlet' valves, but the consequence is only 'Blocked outlet: V-301 level rises...'.
- **Recommendation:** Add 'blocked outlet of the 150# section, liquid settle-out at source pressure' to Dev 1 as a separate consequence. Extend Rec 3 to cover this case at each spec break. Either move each spec break downstream to a relief device sized for blocked outlet and blow-by, or upgrade the new lines and ST-017 to the upstream class up to V-312, or provide an independent PSHH/LSLL trip on the HP-side valve. Lock open the valves downstream of a spec break (CSO/LO) only if the relief calculation supports it.


### A4.3 [Critical] V-312's relief path is not shown and Rec 4 would remove one. No PSV appears on V-312 on P&ID 041: the items next to LSHH/LSLL-1004 are PSD-231/232 shutdown functions. Per 041 Note 5, V-312 runs on a 2" atmospheric cold vent with the LAM-16 flare line closed, and Rec 4 additionally blinds 'V-312 line to the LAM-16 flare while on atmospheric vent'. In a gas blow-by through a 3" line at separator pressure, the 2"-VF-B013-8095-X vent (vent outlet marked about 3 m; stack height on HOLD 1; an isolation valve appears to be fitted at TP-08/09) may be the only path out of V-312. Its capacity, any isolation valve in it, and dispersion of a blow-by gas plume from about 3 m are not assessed.

- **Worksheet ref:** Dev 2 (More Flow) safeguard 2 and consequence 2; Rec 4; Rec 3
- **Evidence:** P&ID 041: vent line 2"-VF-B013-8095-X with DBB PI-550 and '3 METERS APPROX' at the vent outlet; Note 5: 'Vent to ATM shall be operated by closing the line to LAM-16 flare'; HOLD 1 (stack height). The text layer shows 'PSD 232'/'PSD 231' and no PSV tag for V-312. Rec 4 lists blinding of the 'V-312 line to the LAM-16 flare while on atmospheric vent'.
- **Recommendation:** Rec 3 should explicitly size the V-312 relief path, vent or PSV, for the governing cases: LV-303/LCV-304 fail-open gas blow-by at the maximum source pressure, fire, and vapour from flashing. Withdraw the part of Rec 4 that blinds the flare line until Rec 3 shows the vent alone is adequate. Lock open any valve in the vent path (CSO/LO). Complete the HOLD 1 dispersion study for the blow-by rate, not only the normal flash rate.


### A4.4 [Major] The V-100 route has the highest documented source pressure (V-100 DP 55 barg, run close to wellhead pressure), yet it is missing from the blow-by analysis. Dev 10 (Low Level) covers V-301/LSLL-305 only. Rec 3 lists CITHP and the HP header, not V-100 at 55 barg. Rec 10's conditions for using the V-100 route (inspect the LSHH/LSH/LSLL-101B switches, refurbish the valves) do not require the HP/LP calculation or a protection device on the D013/B013 break.

- **Worksheet ref:** Dev 2 cause 1 (LCV-304 wide open); Dev 10; Rec 3; Rec 10
- **Evidence:** Header: 'DP = V-100 55 barg', new lines 150# at 19.6 barg (38 °C). P&ID 030 Note 5 and Note 6 (well 192B selected). Inspection sheet (Test Separator): no LCP on V-100; LV-102B 'Severe corrosion'; IA manifold 'severe corrosion'. Dev 10 cause: 'LV-303 stuck open / LIC-302 fails open'; there is no V-100 equivalent.
- **Recommendation:** Add a separate Low Level / gas blow-by deviation for V-100 (LCV-304 / LV-101B / LV-102B failing open, LSLL-101B uncredited). Add V-100 at 55 barg to the scope of Rec 3, and make a successful Rec 3 result plus a relief or trip device at the D013/B013 break a precondition in Rec 10.


### A4.5 [Major] A single check valve is credited as a hardware safeguard against overpressure from HP to LP, and the scenario is ranked low (E4, RR3). The V-100 oil outlet connects to trunklines in 600#-class piping (4"-PR-D013-103-X / 4"-PR-D013-120-X). If the check valve on 3"-PR-B013-8086-H passes, trunkline pressure reaches the 150# line. API 521 treats check-valve leakage and failure as a credible cause, and a check valve is not an acceptable overpressure protection layer. The worksheet itself says 'existing valves not shown NC'.

- **Worksheet ref:** Dev 4 (Mis-directed Flow) cause 2; Dev 3 safeguard 1
- **Evidence:** Dev 4 cause 2: 'crude at trunkline pressure can back into the new 150# line if the check valve passes'. Safeguards: 'Check valve - hardware. NC philosophy - procedural.' Ranked People E4 RR3. P&ID 030: 'TO BLOCK-1 8" TRUNKLINE 4"-PR-D013-103-X', 'TO LAM-A EXPORT 16" TRUNKLINE 4"-PR-D013-120-X'. The check valve on 8086 is visible on P&ID 031.
- **Recommendation:** Re-rank with People severity based on overpressure of the 150# line (the same severity as Dev 2). Remove the check-valve credit for overpressure. Put the trunkline maximum operating pressure into Rec 3, and require positive isolation of the trunkline connection (Rec 4) as a precondition, not a procedural option.


### A4.6 [Major] An existing direct line from V-301 to V-312, bypassing ST-017, is not addressed. P&ID 031 shows 'TO BULLET TANK 4"-PR-C013-155-X' leaving the V-301 liquid header via FSV-010, BV-023 and valve (024) with PI-002. P&ID 041 shows the matching 'FROM REPCO SEPARATOR 4"-PR-D013-155X3' entering V-312. This is a second, larger route for liquid and gas blow-by into V-312. It also carries unfiltered sand past ST-017, and its class changes (C013 on 031, D013 on 041). It is in neither Rec 4's blind list nor Rec 3.

- **Worksheet ref:** Dev 4 cause 1 (V-301 not fully isolated); Rec 4; Dev 2
- **Evidence:** P&ID 031 text: 'C013 B013 4"-PR-C013-155-X', valve (024), PI-002, to drawing L028-PR-PID-01-M0001-032-00. P&ID 041 text: 'FROM REPCO SEPARATOR 4''-PR-D013-155X3' (4"x3" reducer) into V-312. No mention of line 155 in the worksheet.
- **Recommendation:** Add line 155 as a cause under Dev 2/4. Positively isolate it (blind) for the trial, or include it in the Rec 3 blow-by and relief sizing (combined flow with the 3" route). Clear up the C013/D013 labelling of the line.


### A4.7 [Major] Fire and thermal-expansion relief are not considered at all. ST-017, which has inlet and outlet valves and a locked-closed bypass, and the new 3" lines can be blocked in liquid-full between batches (Rec 12 draining is procedural only) and between the DBB valves at PI-543, PI-545 and PI-546. No thermal relief valve is shown on any new line. The fire case for V-312, a bullet tank holding crude whose relief device is not confirmed, and for ST-017 is also not covered by Rec 3.

- **Worksheet ref:** Rec 3 (scope: 'Gas blow-by and blocked-outlet cases per API 521'); Dev 7; Dev 16/17 (ST-017 isolation)
- **Evidence:** P&ID 031/030/041: no TSV or PSV on 3"-PR-B013-8083/8085/8086/8087-H or ST-017; DBB assemblies at PI-543 (030), PI-545 (031 and 041), PI-546 (041). Rec 3 text lists only blow-by and blocked outlet. Dev 7: 'No heat source in Node 1... Not credible.'
- **Recommendation:** Extend Rec 3 to cover the fire case (V-312, ST-017) and hydraulic expansion of blocked-in liquid (solar gain and hot-oil flushing). Provide TSVs on the isolable sections of the new lines and ST-017, or a justified procedural drain-down with lock-open of one end. Record the outcome in Dev 7 instead of 'not credible'.


### A4.8 [Major] V-312 is designed for 20 barg, which is above the rating of the 150# lines feeding it: 19.6 barg at 38 °C, 17.7 barg at 93 °C, and lower again at the stated 110 °C design temperature. Any V-312 PSV set at or near 20 barg therefore does not protect the inlet lines or ST-017. The header says V-312 governs the design temperature but does not reconcile pressure and temperature: the 150# rating at 110 °C is not given.

- **Worksheet ref:** Design Conditions header ('DT = -29 to 110 °C (V-312 governs)'; 'V-312 20 barg'); Rec 3
- **Evidence:** Header values as quoted. P&ID 041: the inlet from the strainer is '3"-150#' and BV-352 is '6",150#'.
- **Recommendation:** In Rec 3, take the governing design pressure of the low-pressure section as the minimum rating of the 150# components at the maximum coincident temperature (flushing return at 75–80 °C per P&ID 062 Note 5, or 110 °C), and set any V-312 relief at or below that, or justify otherwise. State the 150# rating at 110 °C in the header.


### A4.9 [Major] The V-312 cold vent is shared with existing vent and drain systems, and the effect of blow-by on them is not considered. P&ID 041 ties '2"-VF-B013-5056-X VENT FROM EXISTING OPEN DRAIN TANK' into the new vent, and P&ID 025 ties V-001 (vent/drain drum, 4 m³) into the new cold vent at TP-12A/B. Blow-by into V-312 would raise the vent back-pressure and could push gas into V-001 and the open-drain header (8"-DC-B013-141), releasing it at drain points or overpressuring V-001 (design pressure not shown).

- **Worksheet ref:** Dev 2 consequence 2 ('large gas flow out of the atmospheric vent stack'); Dev 15
- **Evidence:** P&ID 041: 2"-VF-B013-5056-X 'Vent from existing open drain tank, L028-PR-PID-01-M0001-025-00' joining the vent line via a 2"-150# valve. P&ID 025: TP-12A/B 'TO NEW COLD VENT 2"-150#' from V-001's 2"-VA-B013-203-X. HOLD 1 on both drawings.
- **Recommendation:** Add this interaction to Dev 2 (or as a cross-reference to Node 2). Include vent back-pressure and the effect on V-001 and the open-drain system in Rec 3 and the HOLD 1 study, or separate the V-312 vent from the drain-system vent for the trial.


### A4.10 [Major] The H2S content of well 192B is unknown, and Dev 18 itself mentions 'wet sour crude in CS B013 lines', yet nothing checks that the new B013 lines, DBB valves, gaskets and bolting, or the ex-stock ST-017 (P&ID 031 Note 3, 'available in stock'; rating TBC), are suitable for sour service under NACE MR0175 / ISO 15156. Rec 7 sets only an H2S acceptance limit for the fluid.

- **Worksheet ref:** Dev 11 cause 3 (H2S); Dev 18 (Corrosion/Erosion); Rec 7
- **Evidence:** Dev 11 cause 3: 'H2S in the produced fluid (content not stated)'. Dev 18: 'wet sour crude in CS B013 lines'. P&ID 031 Note 3: 'Basket strainer is available in stock'. Header: 'ST-017 TBC'.
- **Recommendation:** Make the H2S partial pressure of well 192B a hold point. Add a recommendation to confirm sour-service compliance and material certificates for the B013 class, ST-017 (design pressure and temperature, hydrotest, nameplate, closure type) and the DBB valves before installation.


### A4.11 [Major] PSV-304A on V-301 is credited without evidence it is serviceable, and its set pressure, which bounds the source pressure the low-pressure section sees, is not recorded. The inspection sheet says only 'available'; for PSV-100B it says 'In good condition and fully functional'. With PSV-304B removed, the position and blinding of its inlet valve (016) is not addressed. Dev 5 says 'PSV-304A lifts to flare' but gives no set pressure to compare against the 150# rating.

- **Worksheet ref:** Dev 1 (blocked-outlet) safeguard 2; Dev 5 safeguard 1 and consequence; Dev 13; Rec 9
- **Evidence:** Repco inspection sheet item 8: 'PSV L028-21-PSV-304A available but L-028-21-PSV-304B is missing in field (sent for yearly calibration)'. P&ID 031: PSV-304A/B with inlet valves (014)/(016) discharging to 3"-PR-B013-149-X and the flare. Worksheet credits 'PSV-304A - vessel only'.
- **Recommendation:** Credit PSV-304A only with a current test or calibration certificate and its recorded set pressure. Include V-301's PSV set pressure plus accumulation as a source-pressure case in Rec 3. Add to Rec 9 that the open PSV-304B inlet is blinded or locked closed under the PSV-isolation procedure.


### A4.12 [Major] Joule-Thomson cooling, two-phase flow and flashing are not considered. Dev 8 covers only ambient wax cooling. When separator pressure is let down across LV-303 or LCV-304 to the near-atmospheric V-312, the crude flashes into two-phase or slug flow in the new 3" line and ST-017. That can cause vibration, hammer and loads on the new flanges. In blow-by, gas expanding from separator pressure can cool by JT effect toward or below the -29 °C design minimum and form hydrates or ice in the vent. None of this appears in the worksheet.

- **Worksheet ref:** Dev 8 (Low Temperature); Dev 2; Rec 3
- **Evidence:** Dev 8 cause: 'Ambient cooling of stagnant waxy crude...'. Header: DT -29 °C minimum. No deviation addresses flashing or two-phase flow; V-312 runs on an atmospheric vent (P&ID 041 Note 5).
- **Recommendation:** Add Low Temperature cause 2 (JT cooling during blow-by or depressurisation) and a two-phase flow / vibration cause. Include the minimum metal temperature during blow-by and the two-phase line and vent hydraulics in Rec 3, and check pipe supports at the new spools and ST-017.


### A4.13 [Major] Hot oil in flushing mode and reverse flow from V-312 are deferred to a node that does not exist. The worksheet sends hot crude returning in flushing mode to 'Node 3 (to be added)', but the Node 1 header already quotes the 93 °C rating, and hot oil at 75–80 °C (P&ID 062 Note 5) can reach the new lines. Dev 3 considers only V-301 to V-100 back-flow. Reverse flow from V-312 into ST-017 and V-301 is not considered: there is no check valve on 3"-PR-B013-8085-H, and V-312 has many inlets, including PSV discharges, LP separator, 25K separator gas and the line heater per P&ID 041. That route could carry hot oil or gas into a depressured or open ST-017 during cleaning.

- **Worksheet ref:** Dev 7 (High Temperature); Dev 3 (Reverse Flow)
- **Evidence:** Dev 7: 'Not credible in filling mode... Node 3 (to be added)'. P&ID 062 Note 5: 'Oil shall be heated to maximum temperature of 75°C-80°C'. P&ID 041 inlets: 'FROM PSV ON QUINTEX PUMPS', 'FROM LP BOOSTER PUMP PSV OULET', 'FROM PUMP PSV', 'FROM LINE HEATER (H-001)'. Note 7: NC applies only 'when bullet tank is used for hot oil operation'.
- **Recommendation:** Make the Node 3 / flushing-mode review a hold point before the trial. Add a Reverse Flow cause (V-312 to ST-017/V-301) with the associated pressure and temperature exposure, and consider a check valve or positive isolation at the V-312 inlet during strainer maintenance.


### A4.14 [Major] Static and ignition are dismissed as 'no incremental concern'. But Dev 4 acknowledges that air can enter V-312 when it runs on the atmospheric vent, which creates a flammable vapour space inside. Filling with crude that carries water and sand, through a new strainer that may not be bonded, generates static. The nitrogen connection that is available (P&ID 041 TP-07, 'NITROGEN CONN') is not used as a safeguard. Gas release from the 3 m vent during blow-by is also an ignition and fire risk in Node 1's direct consequence chain.

- **Worksheet ref:** Dev 15 (Ignition / Static); Dev 4 consequence ('air ingress')
- **Evidence:** Dev 15: '1. Minor release in a classified area; no new ignition source in Node 1.' Dev 4: 'water bottom in V-312 with air ingress'. P&ID 041: TP-07 '(NITROGEN CONN) N4'.
- **Recommendation:** Add an internal-explosion consequence for V-312, with static from filling and air ingress. Recommend nitrogen blanketing or purging of V-312 via TP-07, bonding and earthing of ST-017 and the new spools, an inlet velocity limit or a submerged inlet, and vent ignition / flame-arrester considerations in the HOLD 1 study.


### A4.15 [Minor] The pressure gauge the operator is told to monitor cannot be identified unambiguously. PI-545 appears on two drawings: near TP-04 on P&ID 031 and at the V-312 inlet on P&ID 041. The strainer gauge is an unassigned 'PI-54X'. ST-017 is titled 'A/B' but drawn as a single basket with a 100 % bypass.

- **Worksheet ref:** Dev 1 cause 2 safeguard ('PI-545 / PI-54X'); Rec 11 ('PI-545 read every 10 min')
- **Evidence:** P&ID 031: PI-545 with DBB near TP-04, and 'PI 54X' at ST-017. P&ID 041: PI-545 with DBB at 'OIL FROM BASKET STRAINER'. P&ID 031 title block: 'L028-21-ST-017 A/B'.
- **Recommendation:** Assign unique tags, state which gauge carries the Rec 11 stop limit, and resolve the A/B versus single-basket configuration (this ties to Rec 6).


### A4.16 [Minor] The inspection sheet uses LAM-75 tags for V-301 equipment (LAM75-PV-303, LAM-75-LV-303, old LCP number LAM75-LCP-301). That suggests V-301 or its instruments were moved from another platform. The worksheet does not flag this as a reason to verify the V-301 nameplate, certification and as-built design pressure, which are exactly the missing inputs.

- **Worksheet ref:** Dev 19; header ('V-301 TBC')
- **Evidence:** Repco inspection sheet items 1, 4 and 6: 'Old number (LAM75-LCP-301)', 'LAM-75-LV-303 (As per the available tag)', 'LAM75-PV-303'.
- **Recommendation:** Add to the V-301 design-data hold point: confirm the nameplate, the design pressure and temperature, the last inspection or hydrotest, and the PSV set-pressure consistency for the relocated vessel.


### A4.17 [Observation] The new lines end in '-H' (3"-PR-B013-8083/8085/8086/8087-H), while existing lines end in '-X' or '-E40'. If '-H' is an insulation or heat-conservation code, the statement 'no tracing / insulation shown' may be wrong. This could not be checked because the legend drawing (STDS-PR-PID-1-0001-01-00) was not provided.

- **Worksheet ref:** Dev 8 safeguard ('no tracing / insulation shown')
- **Evidence:** P&ID 031/030/041 line numbers. P&ID 030 shows separate 'INSULATION' / 'NO INSULATION' markings.
- **Recommendation:** Check the line-designation legend and correct Dev 8. If the lines are insulated, consider personnel protection and its effect on the fire/thermal relief case.


## A5. Risk ranking & recommendation quality

**Reviewer summary.** Review lens: risk ranking and recommendation quality, Node 1 HAZOP worksheet (c580b64e-Hot_Oil_Unit_HAZOP_Worksheet-Node_1_completed-10_Nov_2026.docx), checked against the Repco and TDE inspection sheets.

The arithmetic of the risk ranking holds up. I extracted all 200 S/L/RR triplets and every S-L pair maps to one RR (C4=2, C2/C3/D3/D4/E4=3, D2/E2/E3/F2/F3/F4=4). There are no lookup errors.

The weak points are credibility and logic:
(1) The principal HP gas blow-by scenarios (dev 2 and 10) take residual credit of L4 to L2 (RR2 to RR3) from recommendations that are conditional (Rec 3 "if any element cannot withstand"), have an escape clause (Rec 2 "or record formally that no shutdown function exists"), or are deferred analyses (Rec 14 LOPA).
(2) Severity looks understated for blow-by, fire and explosion (People C, Asset D, Reputation E). Burning liquid fall-out (dev 1 cause 2, dev 9) is ranked lower still (People D, Reputation F).
(3) Residual severity is lowered by preventive recommendations in dev 11 cause 1 and dev 4 cause 1, which is a methodology error.
(4) Likelihood is not consistent for the same consequence: loss of instrument air (dev 13) is L3 while dev 10 is L4, and the reduction for dev 9 differs from dev 10.
(5) The LOPA in Rec 14 covers only dev 2 and 10. Other People-C RR2 scenarios are left out, and a SIL requirement is missing for the trip option in Rec 3.
(6) PSV-304A is credited as a hardware safeguard with no test evidence. This contradicts the study's own rule of no credit for untested items.
(7) The recommendations are well written technically but not SMART. There are no due dates, no named owners and no marked pre-start-up hold points. Owners are often joint. Rec 1 is an omnibus recommendation repeated in 8 rows. Rec 8 relies on 'live' validation that cannot happen before the trial.
(8) Rec 4 may blind a relief or vent path from V-312 while the V-312 PSV discharge is unconfirmed.

Overall, the current risk ranking is credible and conservative. The residual ranking is optimistic and should be marked provisional until Rec 2, 3 and 14 close.

**Strengths noted:**

- The S-L-RR lookup is internally consistent across all 200 ranked cells (no arithmetic RAM errors), and the ranking basis is stated explicitly in the header: current = safeguards in reported condition, residual = after recommendations, DO 6x6 RAM, RR1 highest.
- Safeguards are credited realistically against the 03-Nov-2026 inspection sheets. LSHH/LSLL, the LCP and LSHH-101B are marked 'NOT CREDITED', and safeguards are labelled hardware or procedural. This follows the chairman's 27-Oct instruction.
- Remarks are used well to record the reasoning behind a ranking. Examples: dev 1 cause 1 'L4 used ... (draft L5 noted)'; dev 12 'SOP alone does not close RR2'; dev 16 '"no incremental concerns" not accepted'; dev 2 rebuts the draft statement 'overpressure not credible'.
- Rec 2 spots the transposed LSHH/LSLL tags in the inspection sheet. This is confirmed by the Repco sheet items 2 and 3, which show LSHH-305 / LSLL-304, against P&ID tags LSHH-304 / LSLL-305.
- Rec 3 makes a clear technical demand: the 150# line at operating temperature, ST-017, V-312 DP 20 barg and the PSV set pressure checked against CITHP and HP-header pressure, with API 521 blow-by and blocked-outlet cases. It also replaces an unsupported claim with a calculation.
- Rec 14 recognises that the gas blow-by scenario needs LOPA. Rec 11 sets a defined credit condition for operator response ('otherwise not credited'), and Rec 10 offers elimination (blind and exclude the V-100 route) rather than only mitigation.


### A5.1 [Critical] The residual risk for the main HP/LP gas blow-by scenario drops two likelihood steps (People C4 RR2 to C2 RR3; Asset D4 RR3 to D2 RR4; Env/Rep E4 RR3 to E2 RR4). The recommendations that would justify this are not yet defined: they are conditional or deferred, so the residual ranking is not supported.

- **Worksheet ref:** Flow dev 2 (More Flow) cause 1; Level dev 10 (Low Level) cause 1 - Residual Risk columns; Recs 2, 3, 14
- **Evidence:** Rec 3 is conditional: 'If any element cannot withstand the source pressure, provide a PSV ... or an independent LSLL / PSHH trip'. The protection is therefore unknown until the calculation is done. Rec 2 allows 'commission LCP L028-82-LCP-002 or record formally that no shutdown function exists'. Under the second option no LSLL trip exists at all. Rec 14 (LOPA) is to be done 'once Recs 2 and 3 define the available protection', which means after the residual L2 has already been entered. The header shows CITHP 'INPUT REQUIRED' and V-301 DP 'TBC'. The dev 19 remark says 'Inputs still required: well 192B CITHP, V-301 design data, MOC number'.
- **Recommendation:** Mark the dev 2 and dev 10 residual rankings 'PROVISIONAL - pending Rec 3/Rec 14'. Leave residual likelihood at L4 (RR2) until the calculation shows either no overpressure or a defined, tested IPL. Make closure of Rec 3 and Rec 14, with a LOPA outcome that meets the DO target, a formal hold point before the first batch. Re-rank in a HAZOP close-out session.


### A5.2 [Critical] Rec 2 contains an escape clause that could close the action without providing any protection. The residual reductions in five deviations still assume the V-301 trips are restored.

- **Worksheet ref:** Rec 2 (dev 1 cause 2, dev 2, dev 9, dev 10, dev 19)
- **Evidence:** Rec 2: '... commission LCP L028-82-LCP-002 or record formally that no shutdown function exists; function-test with signed records.' The Repco inspection sheet item 1 says the LCP 'has never been put into active service' and its push buttons and lamps are non-functional. Items 2 and 3 say both level switches are 'not functioning and cable found disconnected'. Yet dev 9 residual People goes D4 to D3 and dev 10 residual C4 to C2, partly on the strength of Rec 2.
- **Recommendation:** Split Rec 2 into two parts. 2a: restore the LSHH/LSLL instruments and confirm their final elements (C&I Engineering). 2b: if no shutdown function exists, the scenario must be re-ranked, the residual credit removed, and an alternative independent layer provided (Rec 3 PSV or trip) before the trial. State in the recommendation that the 'no shutdown function' outcome cannot close the action without approval from the HAZOP chairman or Technical Authority.


### A5.3 [Major] Severity looks understated for HP gas blow-by into a vented bullet tank with fire or explosion, and for burning liquid fall-out ('golden rain') on the platform. Similar fire consequences are also ranked differently from one another.

- **Worksheet ref:** Dev 2, dev 4 cause 1, dev 5, dev 10, dev 13 (gas blow-by); dev 1 cause 2 and dev 9 (burning liquid fall-out) - Severity columns
- **Evidence:** Dev 2 consequence: 'GAS BLOW-BY ... large gas flow out of the atmospheric vent stack; LOPC, fire / explosion'. It is ranked People C, Asset D, Reputation E. Dev 1 cause 2 and dev 9 ('burning liquid fall-out on the platform') are ranked People D and Reputation F (RR4). In dev 1 cause 2 Asset is ranked E, against D for dev 9. On an offshore platform, a vapour-cloud explosion or a burning liquid release onto a manned deck can credibly cause multiple fatalities and major asset loss. 'C' may therefore be optimistic. The DO RAM descriptors are not attached to the worksheet, so the exact category cannot be verified.
- **Recommendation:** Attach the DO RAM severity descriptors to the worksheet. Re-rank dev 2, 4, 5, 10 and 13 for credible worst case without safeguards (consider People B and Asset C) and justify any retention of C in Remarks. Rank dev 1 cause 2 and dev 9 consistently with each other and with dev 2, since both are hydrocarbon fire on the platform (People at least C). Rank Reputation for an offshore fire at least E, as dev 2 already does.


### A5.4 [Major] Residual severity is lowered by recommendations that are preventive (they reduce likelihood), which is a methodology error. Severity should reflect the unmitigated consequence and change only through mitigation of the consequence or removal of inventory or hazard.

- **Worksheet ref:** Composition dev 11 cause 1 (sand); Flow dev 4 cause 1 (water to V-312) - Residual vs Current severity
- **Evidence:** Dev 11 cause 1: current People C4 RR2 becomes residual D3 RR3. The consequence is 'fire / explosion, injury / fatality'. Recs 7, 6 and 1 are sampling, strainer and SOP measures, so they reduce likelihood only. Dev 4 cause 1: current People D4 and Asset D4 become residual E3 and E3 after Rec 5, which only asks to 'confirm the destination; if V-312, re-route'.
- **Recommendation:** Restore the residual severity to match current severity (dev 11: People C, residual C3 RR3; dev 4 cause 1: People D, Asset D) and reduce only likelihood. If Rec 5 removes the water line entirely, record the scenario as 'eliminated' in Remarks instead of lowering severity.


### A5.5 [Major] The same consequence is given different likelihoods. Loss of instrument air leading to fail-open LV-303 and gas blow-by is ranked L3 (RR3), while dev 10 is ranked L4 (RR2) for the same outcome. This is despite the dev 13 remark that the corroded IA manifold makes IA loss credible. The residual C2 also relies on recommendations that do not change fail behaviour.

- **Worksheet ref:** Others dev 13 (Loss of Utilities) vs Level dev 10 / Flow dev 2
- **Evidence:** Dev 13: 'Fail-open LV: gas blow-by (deviation 10)'. Current is ranked C3 RR3, E3, D3, E3. Remark: 'Corroded V-100 IA manifold makes IA loss credible'. The TDE sheet item 8 says the 'instrument air manifold has severe corrosion'. The residual is C2 RR3 on Rec 8 ('record the fail position') and Rec 3. Recording a fail-open position does not reduce frequency.
- **Recommendation:** Rank dev 13 current likelihood at least equal to dev 10 (L4, RR2). Add a recommendation to confirm, and if necessary change, the LV-303 fail action to fail-closed (or provide a low-level backup). Include IA failure as an initiating event in the Rec 14 LOPA.


### A5.6 [Major] The LOPA/SIL scope is too narrow. Six People-C RR2 scenarios exist, but LOPA is required for only two. Rec 3 also allows an 'independent LSLL / PSHH trip' as the solution without requiring SIL determination or verification.

- **Worksheet ref:** Rec 14 (dev 2, dev 10 only); Rec 3; RR2 rows dev 4 cause 1, dev 5, dev 11 cause 1, dev 12, dev 19
- **Evidence:** Current RR2 (People C4) appears in dev 2, dev 4 cause 1 (HP header ingress through BV-018), dev 5 (high pressure), dev 10, dev 11 cause 1 (sand to heater, fire), dev 12 (mal-operation) and dev 19. Rec 14 covers 'deviations 2 and 10' only. Rec 3 asks for 'a PSV to safe location or an independent LSLL / PSHH trip before the trial' and gives no SIL target, proof-test interval or bypass control.
- **Recommendation:** Widen Rec 14 to all scenarios with current RR2 or People severity C or worse, including dev 4 cause 1, dev 5, dev 11 cause 1, dev 12, dev 13 and dev 19. Add to Rec 3 that any new trip must have a SIL determined (LOPA/IEC 61511), be designed and verified to that SIL, and be function-tested before start-up. Confirm the DO tolerable frequency (already requested in Rec 14) before the LOPA is closed.


### A5.7 [Major] PSV-304A is credited as a hardware safeguard without any test or calibration evidence. This conflicts with the study's own basis that 'non-functional / untested items not credited'. Rec 9 deals only with PSV-304B.

- **Worksheet ref:** Safeguards column: PSV-304A credited in dev 1 cause 2, dev 4 cause 1, dev 5, dev 13; Rec 9
- **Evidence:** The Repco sheet item 8 says only 'PSV L028-21-PSV-304A available but L-028-21-PSV-304B is missing in field (... sent for yearly calibration)'. There is no set pressure, certificate date or test result for 304A. The worksheet header says 'non-functional / untested items not credited'. Rec 9: 'Reinstate PSV-304B ... or demonstrate ... PSV-304A alone covers the governing relief case'.
- **Recommendation:** Expand Rec 9 to cover: verify the PSV-304A set pressure against the V-301 MAWP, its last test certificate and its inlet/outlet isolation (locked open), and confirm the flare tail-pipe route. Until this evidence is provided, list PSV-304A as 'credit subject to verification' and show the effect on dev 5 and dev 13 ranking.


### A5.8 [Major] No recommendation has a due date, priority or named owner, and pre-start-up hold points are not identified consistently. Only Rec 2, 3 ('before the trial') and 13 ('before the first batch') carry timing. Recs 4, 5, 6, 7, 8, 9, 10, 11, 12 and 14 do not, yet the residual rankings depend on them.

- **Worksheet ref:** All recommendations; Responsibility column
- **Evidence:** Rec 8 asks to 'Refurbish and validate under live conditions LV-303 / LIC-302, PV-303 ...'. Validation under live conditions can only happen during operation, which contradicts using Rec 8 for residual credit in dev 9, dev 13 and dev 18 before the trial. Responsibility entries are departments only (e.g. 'Rec 1: Engineering / Operations').
- **Recommendation:** Add 'Priority / Timing (Pre-start-up hold point / Before batch 2 / Post-trial)' and 'Target date' columns, and name an individual action owner for each recommendation. Mark Recs 1-4, 6, 7, 9, 10, 11, 13 and 14 as PSSR hold points. Rewrite Rec 8 into two parts: (a) refurbish and bench/stroke test before start-up, with a signed record, as the credited part; (b) live validation at first introduction of hydrocarbons, under the Rec 11 manning conditions.


### A5.9 [Major] Operator response is the main barrier to the trip-less V-301 and drives several residual likelihood reductions. However, no process safety time has been established, and some actions in Rec 11 may not be practical for the operator stationed at V-301.

- **Worksheet ref:** Rec 11 (dev 1 cause 2, dev 2, dev 9, dev 12) - operator response credit
- **Evidence:** Rec 11: 'PI-545 read every 10 min against a stop limit from Rec 3; response time to any deviation not more than 5 min ... close well 192B choke at high mark'. Loss of liquid seal through a stuck-open LV-303 (dev 10) can develop in less time than a 10-minute reading interval. The worksheet gives no evidence that the V-301 operator can reach the 192B choke. Rec 11 also depends on Rec 3 for the stop limit.
- **Recommendation:** Ask Rec 3 to calculate the V-301 level drain-down time and the process safety time for blow-by and high level. Allow the Rec 11 operator response to be credited only if the detection-plus-response time is less than half the PST. Confirm who closes the 192B choke and that a person is present at it. Make the reading interval or continuous attendance follow from the PST, rather than a fixed 10 minutes.


### A5.10 [Major] Rec 4 asks for a spectacle blind on the V-312 line to the LAM-16 flare. Dev 2 states that the V-312 PSV 'tag / set / discharge NOT CONFIRMED'. If that PSV, or the blow-by relief case, discharges into this line, the blind would defeat the last line of overpressure protection.

- **Worksheet ref:** Rec 4 (dev 4 cause 1, dev 4 cause 2, dev 12) - 'V-312 line to the LAM-16 flare while on atmospheric vent'; dev 2 safeguard 2
- **Evidence:** Rec 4: '... V-312 line to the LAM-16 flare while on atmospheric vent'. Dev 2 safeguard 2: 'V-312 PSV: tag / set / discharge NOT CONFIRMED'. Rec 3 relies on the 'V-312 PSV set'.
- **Recommendation:** Make Rec 4 conditional on Rec 3 confirming the V-312 PSV discharge route and that the atmospheric vent is sized for the gas blow-by case (API 521 / API 2000). Do not blind any line that forms part of a relief path. Record the result in the blind register and the PSV register.


### A5.11 [Major] H2S exposure is ranked inconsistently and without data. The H2S content of well 192B is unknown, yet People severity varies between rows. The residual is reduced by sampling alone, and no recommendation requires the H2S data before the trial or calls for detection.

- **Worksheet ref:** Composition dev 11 cause 3 (H2S); Others dev 14 (Sampling); Others dev 16 (Drainage) - People severity
- **Evidence:** Dev 11 cause 3 has People D4 RR3 and residual D3. Dev 14 ('exposure to H2S / hydrocarbons at the sample point') has People E3 RR4. Dev 16 ('H2S exposure while cleaning the basket') has People E3 RR4. The dev 11 cause 3 cause reads 'H2S ... content not stated', and the safeguard is 'Personal H2S monitors - procedural'. Rec 7 only sets an 'H2S' acceptance limit.
- **Recommendation:** Add a recommendation (owner: Production Chemistry, before the trial) to measure the H2S content of the 192B gas and liquid. Rank all H2S exposure rows on one basis at worst-case concentration, until data is available. Make specific requirements for sample-point, DBB-bleed and strainer-opening tasks: portable gas detection, breathing apparatus (BA) criteria and closed sampling. Feed the result into the Node 2 vent dispersion assessment.


### A5.12 [Minor] Similar recommendations produce inconsistent likelihood reductions. Both rows rely on Rec 2 restoring the matching level switch (LSHH-304 for dev 9, LSLL-305 for dev 10), plus operator measures. Dev 9 is reduced L4 to L3, while dev 10 is reduced L4 to L2.

- **Worksheet ref:** Level dev 9 vs Level dev 10 - residual likelihood
- **Evidence:** Dev 9 residual is D3 RR3, E3, E3, F3 with Recs 2, 8 and 11. Dev 10 residual is C2 RR3, E2, D2, E2 with Recs 3, 2 and 14. Rec 3 and Rec 14 add analysis, not a layer of protection.
- **Recommendation:** Apply one rule for likelihood reduction: one likelihood step per credited, independent and tested layer. Re-rank both rows on that rule and state the credited layers in Remarks.


### A5.13 [Minor] Several owners are joint or do not match the work involved. This weakens accountability and closure.

- **Worksheet ref:** Responsibility column: Recs 1, 2, 4, 6, 7, 10, 17
- **Evidence:** Joint owners: Rec 1 'Engineering / Operations', Rec 4 'Engineering / Operations', Rec 7 'Operations / Production Chemistry', Rec 10 'Engineering / Operations'. Rec 2 is assigned to Maintenance, although it includes 'identify and implement their final element from the Repco C&E ... or record formally that no shutdown function exists', which are C&I engineering and Technical Authority decisions. In dev 17, Rec 6 (Engineering) is the only recommendation, although positive isolation and bleed-proofing under PTW is an Operations responsibility.
- **Recommendation:** Give each recommendation one accountable owner (a named role or person), with contributors listed separately. Assign Rec 2 to C&I Engineering, with Maintenance executing. Add Operations as owner of the isolation and bleed-proof procedure in dev 17.


### A5.14 [Minor] Some recommendations are omnibus or duplicated. Rec 1 bundles at least five actions (SOP, line-up verification, blind status, level/pressure limits, batch cap) and is credited for likelihood reduction in eight different scenarios, which makes closure hard to verify. Rec 6 and Rec 12 both ask for the drain destination to be confirmed.

- **Worksheet ref:** Rec 1 (8 rows: dev 1 causes 1 and 2, dev 1 cause 2 (strainer), dev 3, dev 4 causes 1 and 2, dev 11, dev 12, dev 14); Rec 6 vs Rec 12
- **Evidence:** Rec 1 text repeated verbatim across rows. Rec 6: 'drain destination for sand and crude'. Rec 12: 'drain destination to be confirmed'. Dev 16 cites both.
- **Recommendation:** Split Rec 1 into separately verifiable sub-actions (1a SOP, 1b signed line-up checklist, 1c operating limits and stop actions, 1d batch limit). Keep the drain-destination action in one recommendation only, owned by Engineering, with the destination specified (closed drain or open drain) and its H2S implications.


### A5.15 [Minor] Open inputs are recorded in Remarks rather than as actions, and some standard pre-start-up items are missing. No recommendation obtains the V-301 design data or the MOC number, and none requires a leak or pressure test of the new 3" B013 150# lines and flanges, which dev 15 identifies as new leak sources.

- **Worksheet ref:** Others dev 19 Remarks; header (MOC number, V-301 design data); dev 15 (Ignition)
- **Evidence:** Dev 19 remark: 'Inputs still required: well 192B CITHP, V-301 design data, MOC number'. Only CITHP is picked up, in Rec 3. Dev 15: 'New flanged joints, DBB bleeds and strainer cover - leak sources'. Recommendation column '-'. Searching the worksheet text finds no 'pressure test', 'leak test' or 'hydro' entries.
- **Recommendation:** Add recommendations to: (a) obtain the V-301 nameplate/U1A data (MAWP, design temperature) and the MOC number before the HAZOP is closed; (b) hydro/leak-test the new lines, ST-017 and tie-ins, with a test record attached to the PSSR. Re-rank dev 15 once these are in place.


### A5.16 [Observation] Environmental and Reputation rankings barely vary. Almost every row is E or F, including fire/explosion and 'Hydrocarbon / sand to deck or sea' (dev 16, Env E). This suggests these dimensions were not assessed on their own merits.

- **Worksheet ref:** Environmental and Reputation columns (dev 2, dev 10, dev 11 cause 1, dev 16)
- **Evidence:** Dev 2 Env E4 / Rep E4. Dev 11 cause 1 Env E4 / Rep F4 for a heater fire or explosion. Dev 16 Env E3 for discharge to sea. Dev 1 cause 2 Rep F4 for burning liquid fall-out.
- **Recommendation:** Check Environmental and Reputation against the DO RAM descriptors, particularly for a marine release (dev 16) and an offshore fire (dev 1 cause 2, dev 9, dev 11). Record the reason in Remarks where E or F is kept.


### A5.17 [Observation] Several People-C scenarios stay at residual RR3 with no ALARP statement. For a temporary three-batch trial using a vessel whose protections have never been commissioned, the record should state why RR3 is tolerable, or whether the trial should be deferred.

- **Worksheet ref:** Residual Risk - People C scenarios (dev 2, dev 4 cause 1, dev 5, dev 10, dev 12, dev 13, dev 19)
- **Evidence:** Residual C2/C3 RR3 in dev 2, 4, 5, 10, 12, 13 and 19. Rec 14 'confirm the DO target frequency band for People-C scenarios' shows the tolerability criterion is not yet known.
- **Recommendation:** Add an ALARP or tolerability statement for each residual RR3 People-C scenario after the LOPA is done. Consider an overall Node 1 'go / no-go' recommendation tied to closure of Recs 2, 3, 9 and 14.

