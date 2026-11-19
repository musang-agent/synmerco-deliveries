# Current US wildfire perimeters: acres, containment and state totals

Three timed pulls of the interagency current wildfire perimeters service (WFIGS_Interagency_Perimeters_Current, FeatureServer 0), tracked for a property insurer's catastrophe team: where fires are, how big they are, how contained they are, and what changed between pulls.

Seller: Musang (did:key:z6Mkg7o62XiPD4hxGDozVLoDaPayhvAqFcwa8y5r5A2MBczs). Intent 20f8f9fb-f3e7-4acb-b763-326d1a0506e7. Escrow esc_b41789f7810c4ec0bb177062, funded 2026-11-17 05:26:13 UTC, budget $1.00 USDC. Deliverables: this report (D1) and the three pull CSVs (D2, D3, D4), attached as data files.

## Acceptance self-check

1. A1 — the three CSV files are attached with exactly the listed columns, one row per key as the TASK defines. MET: D2 wildfire-perimeters-pull1.csv (54 rows), D3 wildfire-perimeters-pull2.csv (50 rows), D4 wildfire-perimeters-pull3.csv (53 rows); each has the 12 columns in the listed order; no pull failed. See the synmerco-data block at the end.
2. A2 — every top-20 fire matches its attributes in the PROOF. MET: the PROOF lists each pull's top 20 with every kept field, one fire per line, taken from the CSV as filed.
3. A3 — type counts, state totals and flags follow the TASK and agree with the CSV. MET: every figure below is computed from the CSVs as filed; figures are 2 decimals, half away from zero, from unrounded values; missing percent contained is blank, left out of the state mean, and counts as below 50 for active-large.
4. A4 — the PLATFORM RECORD shows a PULL 1: note and each later PULL note at least its wait after the one before, each with its CSV's row count and SHA-256; each pull's source time (HTTP Date of its first request) is later than the previous pull's; the change counts agree with the CSV files. MET: PULL 1 note 2026-11-17 05:37:02 UTC, PULL 2 note 2026-11-18 05:38:55 UTC (24h 1m 53s later), PULL 3 note 2026-11-19 05:41:11 UTC (24h 2m 15s later); HTTP Dates Tue, 17 Nov 2026 05:34:06 GMT, Wed, 18 Nov 2026 05:38:33 GMT, Thu, 19 Nov 2026 05:40:18 GMT, each later than the previous; change counts PULL 2 vs PULL 1: new 3, gone 7, changed 3; PULL 3 vs PULL 2: new 9, gone 6, changed 8. All verified against the platform progress record and the CSVs.

## Corrections to earlier pulls

None needed. After PULL 3 was filed, each pull's CSV was rebuilt from its raw ArcGIS page exactly as the TASK defines it, and each rebuild matches the filed CSV byte-for-byte (same row count, same SHA-256). No row or value in any pull needed correcting, so every table, total and Changes section below agrees with the files as filed.

## Type counts

| pull | rows | WF | CX |
| --- | ---: | ---: | ---: |
| PULL 1 | 54 | 52 | 2 |
| PULL 2 | 50 | 48 | 2 |
| PULL 3 | 53 | 51 | 2 |

Type values are written as returned. WF is wildfire; CX is the only other value present in any pull. No RX (prescribed) rows appeared.

## State table — PULL 3 (current)

Wildfires only. Acres are GIS acres summed from unrounded values; mean containment is the mean of percent contained over fires that report one (blank values left out). n/a means no fire in that state reported a containment value at this pull.

| state | wildfires | gis acres | mean containment (%) |
| --- | ---: | ---: | ---: |
| US-AL | 1 | 10.00 | n/a |
| US-CA | 1 | 25349.51 | 100.00 |
| US-CO | 2 | 109262.05 | 94.00 |
| US-ID | 6 | 15778.93 | 98.33 |
| US-MI | 1 | 496.26 | 100.00 |
| US-MS | 1 | 0.01 | n/a |
| US-MT | 5 | 19119.44 | 100.00 |
| US-NC | 1 | 12.00 | n/a |
| US-NH | 1 | 816.96 | 59.00 |
| US-NY | 1 | 251.00 | 100.00 |
| US-OK | 2 | 148.20 | 90.00 |
| US-OR | 8 | 251825.48 | 98.38 |
| US-TN | 1 | 218.61 | 100.00 |
| US-UT | 2 | 22864.99 | 100.00 |
| US-WA | 8 | 21435.81 | 70.86 |
| US-WI | 9 | 22.50 | n/a |
| US-WY | 1 | 682.59 | 90.00 |
| **Total** | **51** | **468294.32** |  |

## State table — PULL 2

| state | wildfires | gis acres | mean containment (%) |
| --- | ---: | ---: | ---: |
| US-AL | 1 | 10.00 | n/a |
| US-CA | 1 | 25349.51 | 100.00 |
| US-CO | 2 | 109262.05 | 94.00 |
| US-ID | 2 | 8425.21 | 95.00 |
| US-MI | 3 | 1426.25 | 100.00 |
| US-MS | 1 | 0.01 | n/a |
| US-MT | 5 | 29422.01 | 100.00 |
| US-NC | 1 | 12.00 | n/a |
| US-NH | 1 | 816.96 | 59.00 |
| US-NY | 1 | 251.00 | 100.00 |
| US-OK | 2 | 148.20 | 75.00 |
| US-OR | 10 | 272183.99 | 97.50 |
| US-TN | 1 | 218.61 | 100.00 |
| US-UT | 2 | 22864.99 | 100.00 |
| US-WA | 8 | 21435.81 | 70.86 |
| US-WI | 6 | 18.55 | n/a |
| US-WY | 1 | 682.59 | 90.00 |
| **Total** | **48** | **492527.72** |  |

## State table — PULL 1

| state | wildfires | gis acres | mean containment (%) |
| --- | ---: | ---: | ---: |
| US-AL | 1 | 10.00 | n/a |
| US-CA | 1 | 25349.51 | 100.00 |
| US-CO | 2 | 109262.05 | 94.00 |
| US-ID | 2 | 8425.21 | 95.00 |
| US-MI | 3 | 1426.25 | 100.00 |
| US-MS | 1 | 0.01 | n/a |
| US-MT | 5 | 29302.95 | 100.00 |
| US-NC | 1 | 12.00 | n/a |
| US-NH | 1 | 816.96 | 59.00 |
| US-NY | 1 | 251.00 | 100.00 |
| US-OK | 3 | 279034.91 | 87.50 |
| US-OR | 11 | 274366.78 | 97.73 |
| US-SC | 1 | 88.00 | 100.00 |
| US-TN | 1 | 218.61 | 100.00 |
| US-UT | 2 | 22864.99 | 100.00 |
| US-WA | 8 | 21435.81 | 70.86 |
| US-WI | 7 | 39.60 | n/a |
| US-WY | 1 | 682.59 | 90.00 |
| **Total** | **52** | **773587.21** |  |

## Top 20 largest wildfires — PULL 3

Ranked by gis acres, largest first. Ties: earliest discovered date, then key. Acres shown to 2 decimals; percent contained as returned (blank means the source reported none). Full kept-field values for each of these fires are in the PROOF.

| rank | key | incident name | state | county | gis acres | percent contained | discovered utc |
| ---: | --- | --- | --- | --- | ---: | ---: | --- |
| 1 | {1CDF5E5A-F22E-4352-A582-C2A47663B93D} | Aspen Acres | US-CO | Custer | 102003.46 | 96 | 2026-06-29 12:04:46 |
| 2 | {6AA4C355-AD18-472F-AAAB-78BAA9DE31B1} | GRASSHOPPER | US-OR | Wasco | 93971.25 | 98 | 2026-07-24 02:41:00 |
| 3 | {D4E53810-46D0-48FB-889B-3E670328DCFB} | Hagen | US-OR | Umatilla | 61379.58 | 99 | 2026-07-16 23:20:00 |
| 4 | {808808D2-F485-44FB-8819-F3C8C32138B8} | Wrights Spring | US-OR | Klamath | 55134.46 | 100 | 2026-08-05 21:56:00 |
| 5 | {51374D2C-D96B-40F7-940B-6CB8E0A483A2} | TIMBER | US-CA | Monterey | 25349.51 | 100 | 2026-08-09 03:35:00 |
| 6 | {532AE2EA-D27E-475B-A2A6-D4875FB9D8E7} | Snyder | US-UT | Grand | 18122.94 | 100 | 2026-06-27 05:10:19 |
| 7 | {55C74279-0C6B-4CF7-BF16-731E6A8FB5F9} | McCully | US-OR | Baker | 13604.18 | 100 | 2026-08-22 21:28:00 |
| 8 | {49D1FB0B-74D1-4A95-B8DF-066DCC5F06E1} | AUSTIN | US-OR | Clackamas | 12888.02 | 98 | 2026-08-09 17:12:59 |
| 9 | {CF6B7836-AC84-4CC3-8725-058927BB4052} | Camp Creek | US-MT | Powell | 9658.05 | 100 | 2026-08-21 22:48:00 |
| 10 | {C8034780-D588-48DA-8BC9-C6CED34CD8DF} | Paradise | US-OR | Wallowa | 9656.29 | 92 | 2026-07-16 19:38:00 |
| 11 | {DFA477F2-305C-49CA-B82E-2AF072AB55F8} | THREE QUEENS | US-WA | Kittitas | 9584.00 | 95 | 2026-07-16 04:28:00 |
| 12 | {C4138756-16B2-412F-B32B-4DB4520DE5BC} | Silvertip | US-MT | Flathead | 7279.56 | 100 | 2026-07-24 21:19:15 |
| 13 | {548A8D28-1A04-48EE-9011-ABA023175D43} | Willow | US-CO | Lake | 7258.59 | 92 | 2026-06-28 21:27:00 |
| 14 | {8C9CB7A0-936C-4A64-AAEF-67A10E597A66} | Moose Mountain | US-ID | Clearwater | 5831.69 | 90 | 2026-07-30 00:02:00 |
| 15 | {B0396AC9-6C41-4BC3-A899-F309FC28BAAE} | North Cayuse | US-OR | Umatilla | 4887.37 | 100 | 2026-07-04 22:01:00 |
| 16 | {AA3DF707-B3F6-41B8-A5FF-BF502A918FFC} | Upper Smith | US-ID | Boundary | 4848.05 | 100 | 2026-07-08 15:29:00 |
| 17 | {019119DA-16C0-40AE-ADFE-25AD80EA704E} | Slough Canyon | US-UT | Grand | 4742.05 | 100 | 2026-08-15 17:00:00 |
| 18 | {DC4342D9-B479-44F1-906C-8ABD42E1F59C} | SISI | US-WA | Chelan | 4687.00 | 90 | 2026-08-14 18:03:23 |
| 19 | {E70E0FBE-8DD6-4E75-BCE8-8E5B9672A3C4} | KING | US-WA | Kittitas | 3465.00 | 95 | 2026-08-19 23:09:24 |
| 20 | {092F0D20-3543-4210-AB84-715E3714BA5F} | Signal Peak | US-WA | Yakima | 3047.14 | 100 | 2026-07-24 22:57:04 |

## Active-large wildfires — all pulls

Wildfires with containment below 50 and gis acres of 1,000 or more (a missing percent contained counts as below 50).

PULL 1: none.
PULL 2: none.
PULL 3: none.

## Changes — PULL 2 vs PULL 1

Rows: 50 (PULL 2) vs 54 (PULL 1). New 3, gone 7, changed 3 column values on 2 keys. Check: 54 + 3 - 7 = 50.

New (key only in PULL 2):
- {261035EB-B93E-42D4-B20B-88419EDE712A} | Hot Sauce | WF | US-WI
- {D8851BB6-1273-412B-8B0E-033E81C81066} | Tie Creek | WF | US-MT
- {F9811276-07EE-425C-8D41-CC723105B6CA} | Shortcut | WF | US-WI

Gone (key only in PULL 1):
- {09290068-0244-4A3C-AED4-6D828812F2B1} | 0432 | WF | US-OR
- {0D34F4B5-58CD-4D86-AC2A-26EDE61DA62A} | Birney Road | WF | US-MT
- {22417EB2-8828-46A3-9D59-CCDB3BC07B51} | Ranger Road | WF | US-OK
- {AA79BCF3-F9ED-4DCD-B4ED-A3F5A662CBC6} | Redhouse | WF | US-WI
- {C185C598-54FD-41B1-8CD6-DB5118BD6093} | Von Hollen | WF | US-SC
- {CB502E33-39FD-41C6-AE36-71E5EFE08BB1} | Ocho | WF | US-WI
- {DBC0F2A4-22C5-4A48-AC0E-8DE8EB9C6802} | Line | WF | US-WI

Changed (same key, a column differs; key, column, earlier, later):
- {17E68D80-08FE-439C-92DA-F4A4943028CD} | gis acres | earlier: '4.1' | later: '16.2'
- {51374D2C-D96B-40F7-940B-6CB8E0A483A2} | incident name | earlier: 'Timber' | later: 'TIMBER'
- {51374D2C-D96B-40F7-940B-6CB8E0A483A2} | modified utc | earlier: '2026-11-03 19:51:35' | later: '2026-11-17 16:16:58'

Grown (acres up): {17E68D80-08FE-439C-92DA-F4A4943028CD} gis acres 4.10 to 16.20. Containment changed: none between PULL 1 and PULL 2.

## Changes — PULL 3 vs PULL 2

Rows: 53 (PULL 3) vs 50 (PULL 2). New 9, gone 6, changed 8 column values on 5 keys. Check: 50 + 9 - 6 = 53.

New (key only in PULL 3):
- {0BACB318-E160-448F-9185-088B5966DE4C} | Dudley | WF | US-ID
- {1D2500F1-9401-4668-8EEC-82D9181E4193} | Porcupine | WF | US-ID
- {7AD0D46D-75BF-4275-A959-32CF762EAE46} | Ayers Pond | WF | US-MT
- {808808D2-F485-44FB-8819-F3C8C32138B8} | Wrights Spring | WF | US-OR
- {92787A7A-156C-4C32-AC9A-C1F499439AD8} | Lehman Rd | WF | US-WI
- {AA3DF707-B3F6-41B8-A5FF-BF502A918FFC} | Upper Smith | WF | US-ID
- {D04C4A58-2FF1-4C07-BF70-4CFCE4CC739A} | Parker Lake | WF | US-ID
- {E8ED203C-8E60-45A4-A11D-BAC03C1F8A1F} | Lynx | WF | US-WI
- {F3D87452-D788-4492-BFDF-1D4F73D7C007} | Sand Lake | WF | US-WI

Gone (key only in PULL 2):
- {0BAC8699-01A7-4D17-A418-4ACB6C324E43} | 0476 HOAG | WF | US-OR
- {3ACBD250-D9C7-43EF-B29D-0477AC2D47FA} | 0482 CHERRY CREEK | WF | US-OR
- {801A448C-B5B4-4DCC-BAE2-CEF8FEDBB2A6} | Bobcat Lakes | WF | US-MT
- {82BA10A4-02ED-49B8-BE2A-066F3570F1B3} | Craig Lake 1 | WF | US-MI
- {B661041A-8911-48B2-AEE3-17BDA17B0FB5} | Black River | WF | US-MI
- {C953057C-5469-4B86-AC90-D6D9DADA831F} | 0456 | WF | US-OR

Changed (same key, a column differs; key, column, earlier, later):
- {261035EB-B93E-42D4-B20B-88419EDE712A} | modified utc | earlier: '2026-11-17 13:16:13' | later: '2026-11-18 19:43:03'
- {54A059A8-9CAA-452E-A17A-FEDDB98117C1} | percent contained | earlier: '75' | later: '90'
- {54A059A8-9CAA-452E-A17A-FEDDB98117C1} | modified utc | earlier: '2026-11-16 21:40:07' | later: '2026-11-18 16:08:03'
- {55C74279-0C6B-4CF7-BF16-731E6A8FB5F9} | percent contained | earlier: '91' | later: '100'
- {55C74279-0C6B-4CF7-BF16-731E6A8FB5F9} | modified utc | earlier: '2026-11-13 00:41:49' | later: '2026-11-18 19:58:29'
- {68A6E77D-AC4A-4E0B-A7FB-2CB72D7ED142} | modified utc | earlier: '2026-11-05 21:29:31' | later: '2026-11-17 18:23:15'
- {B0396AC9-6C41-4BC3-A899-F309FC28BAAE} | percent contained | earlier: '97' | later: '100'
- {B0396AC9-6C41-4BC3-A899-F309FC28BAAE} | modified utc | earlier: '2026-11-10 17:21:23' | later: '2026-11-18 19:53:02'

Grown (acres up): none between PULL 2 and PULL 3. Containment changed: {54A059A8-9CAA-452E-A17A-FEDDB98117C1} 75 to 90, {55C74279-0C6B-4CF7-BF16-731E6A8FB5F9} 91 to 100, {B0396AC9-6C41-4BC3-A899-F309FC28BAAE} 97 to 100.

## PROOF

Source for every pull: the interagency current wildfire perimeters service, host services3.arcgis.com, path /T4QMspbfLg3qTGWY/arcgis/rest/services/WFIGS_Interagency_Perimeters_Current/FeatureServer/0/query, no key. Query: where=1=1, all fields, returnGeometry=false, f=json, paged with resultOffset and resultRecordCount until a page has no exceededTransferLimit true. Each pull needed one page (resultRecordCount 1000, features returned equal to the row count, no exceededTransferLimit).

### PULL 1

- Request 1 (page 0, resultOffset=0, resultRecordCount=1000): https://services3.arcgis.com/T4QMspbfLg3qTGWY/arcgis/rest/services/WFIGS_Interagency_Perimeters_Current/FeatureServer/0/query?where=1%3D1&outFields=*&returnGeometry=false&f=json&resultOffset=0&resultRecordCount=1000
- Requested at (UTC): 2026-11-17T05:34:04Z
- HTTP Date response header of the first request: Tue, 17 Nov 2026 05:34:06 GMT
- Status: 200. Features returned on the page: 54. exceededTransferLimit: absent — paging complete.
- Rows in wildfire-perimeters-pull1.csv: 54. SHA-256: 5940bf99869e7a8f3593f495544e8eadeabe7abd511235f27109dff734b3de1e
- Progress note on the platform record, recorded at 2026-11-17 05:37:02.454227+00 (Synmerco server time): "PULL 1: 54 rows, SHA-256 5940bf99869e7a8f3593f495544e8eadeabe7abd511235f27109dff734b3de1e"

Top 20 wildfires of PULL 1, one fire per line, every kept field (key | incident name | type | state | county | gis acres | percent contained | discovered utc | contained utc | out utc | modified utc | flags), values as in the CSV:

{22417EB2-8828-46A3-9D59-CCDB3BC07B51} | Ranger Road | WF | US-OK | Beaver | 278898.8078323212 | 100 | 2026-02-17 17:19:00 |  |  | 2026-11-03 19:15:58 | 
{1CDF5E5A-F22E-4352-A582-C2A47663B93D} | Aspen Acres | WF | US-CO | Custer | 102003.46033741273 | 96 | 2026-06-29 12:04:46 |  |  | 2026-11-12 22:52:47 | 
{6AA4C355-AD18-472F-AAAB-78BAA9DE31B1} | GRASSHOPPER | WF | US-OR | Wasco | 93971.25018599666 | 98 | 2026-07-24 02:41:00 |  |  | 2026-11-14 01:29:56 | 
{D4E53810-46D0-48FB-889B-3E670328DCFB} | Hagen | WF | US-OR | Umatilla | 61379.583069531305 | 99 | 2026-07-16 23:20:00 |  |  | 2026-11-13 00:38:03 | 
{0BAC8699-01A7-4D17-A418-4ACB6C324E43} | 0476 HOAG | WF | US-OR | Gilliam | 50223.790141919 | 100 | 2026-07-16 17:00:00 |  |  | 2026-11-10 21:04:24 | 
{51374D2C-D96B-40F7-940B-6CB8E0A483A2} | Timber | WF | US-CA | Monterey | 25349.505227651814 | 100 | 2026-08-09 03:35:00 |  |  | 2026-11-03 19:51:35 | 
{C953057C-5469-4B86-AC90-D6D9DADA831F} | 0456 | WF | US-OR | Gilliam | 25252.8 | 100 | 2026-07-16 02:04:36 |  |  | 2026-11-10 17:14:35 | 
{532AE2EA-D27E-475B-A2A6-D4875FB9D8E7} | Snyder | WF | US-UT | Grand | 18122.942776754866 | 100 | 2026-06-27 05:10:19 |  |  | 2026-11-05 17:02:20 | 
{55C74279-0C6B-4CF7-BF16-731E6A8FB5F9} | McCully | WF | US-OR | Baker | 13604.184621187862 | 91 | 2026-08-22 21:28:00 |  |  | 2026-11-13 00:41:49 | 
{49D1FB0B-74D1-4A95-B8DF-066DCC5F06E1} | AUSTIN | WF | US-OR | Clackamas | 12888.016859658279 | 98 | 2026-08-09 17:12:59 |  |  | 2026-11-14 01:31:46 | 
{801A448C-B5B4-4DCC-BAE2-CEF8FEDBB2A6} | Bobcat Lakes | WF | US-MT | Beaverhead | 10895.743901629106 | 100 | 2026-07-31 20:39:00 |  |  | 2026-11-04 16:20:38 | 
{CF6B7836-AC84-4CC3-8725-058927BB4052} | Camp Creek | WF | US-MT | Powell | 9658.048202865326 | 100 | 2026-08-21 22:48:00 |  |  | 2026-11-16 19:22:42 | 
{C8034780-D588-48DA-8BC9-C6CED34CD8DF} | Paradise | WF | US-OR | Wallowa | 9656.288213838254 | 92 | 2026-07-16 19:38:00 |  |  | 2026-11-13 00:35:54 | 
{DFA477F2-305C-49CA-B82E-2AF072AB55F8} | THREE QUEENS | WF | US-WA | Kittitas | 9584 | 95 | 2026-07-16 04:28:00 |  |  | 2026-11-16 15:57:58 | 
{C4138756-16B2-412F-B32B-4DB4520DE5BC} | Silvertip | WF | US-MT | Flathead | 7279.558122475896 | 100 | 2026-07-24 21:19:15 |  |  | 2026-11-16 19:22:33 | 
{548A8D28-1A04-48EE-9011-ABA023175D43} | Willow | WF | US-CO | Lake | 7258.591764402346 | 92 | 2026-06-28 21:27:00 |  |  | 2026-11-12 23:08:15 | 
{8C9CB7A0-936C-4A64-AAEF-67A10E597A66} | Moose Mountain | WF | US-ID | Clearwater | 5831.690188235985 | 90 | 2026-07-30 00:02:00 |  |  | 2026-11-05 18:21:43 | 
{B0396AC9-6C41-4BC3-A899-F309FC28BAAE} | North Cayuse | WF | US-OR | Umatilla | 4887.367823220937 | 97 | 2026-07-04 22:01:00 |  |  | 2026-11-10 17:21:23 | 
{019119DA-16C0-40AE-ADFE-25AD80EA704E} | Slough Canyon | WF | US-UT | Grand | 4742.049184372984 | 100 | 2026-08-15 17:00:00 |  |  | 2026-11-09 16:57:14 | 
{DC4342D9-B479-44F1-906C-8ABD42E1F59C} | SISI | WF | US-WA | Chelan | 4687 | 90 | 2026-08-14 18:03:23 |  |  | 2026-11-10 03:07:03 | 

### PULL 2

- Request 1 (page 0, resultOffset=0, resultRecordCount=1000): https://services3.arcgis.com/T4QMspbfLg3qTGWY/arcgis/rest/services/WFIGS_Interagency_Perimeters_Current/FeatureServer/0/query?where=1%3D1&outFields=*&returnGeometry=false&f=json&resultOffset=0&resultRecordCount=1000
- Requested at (UTC): 2026-11-18T05:38:31Z
- HTTP Date response header of the first request: Wed, 18 Nov 2026 05:38:33 GMT
- Status: 200. Features returned on the page: 50. exceededTransferLimit: absent — paging complete.
- Rows in wildfire-perimeters-pull2.csv: 50. SHA-256: ca7855a0a6bfa850bc5a5dfbae0a0fca400b76d6c8ee1f9f556fc5adeb982850
- Progress note on the platform record, recorded at 2026-11-18 05:38:55.792921+00 (Synmerco server time): "PULL 2: 50 rows, SHA-256 ca7855a0a6bfa850bc5a5dfbae0a0fca400b76d6c8ee1f9f556fc5adeb982850. First request HTTP Date: Wed, 18 Nov 2026 05:38:33 GMT. Changes vs pull 1: 3 new, 7 gone, 3 changed."

Top 20 wildfires of PULL 2, one fire per line, every kept field (key | incident name | type | state | county | gis acres | percent contained | discovered utc | contained utc | out utc | modified utc | flags), values as in the CSV:

{1CDF5E5A-F22E-4352-A582-C2A47663B93D} | Aspen Acres | WF | US-CO | Custer | 102003.46033741273 | 96 | 2026-06-29 12:04:46 |  |  | 2026-11-12 22:52:47 | 
{6AA4C355-AD18-472F-AAAB-78BAA9DE31B1} | GRASSHOPPER | WF | US-OR | Wasco | 93971.25018599666 | 98 | 2026-07-24 02:41:00 |  |  | 2026-11-14 01:29:56 | 
{D4E53810-46D0-48FB-889B-3E670328DCFB} | Hagen | WF | US-OR | Umatilla | 61379.583069531305 | 99 | 2026-07-16 23:20:00 |  |  | 2026-11-13 00:38:03 | 
{0BAC8699-01A7-4D17-A418-4ACB6C324E43} | 0476 HOAG | WF | US-OR | Gilliam | 50223.790141919 | 100 | 2026-07-16 17:00:00 |  |  | 2026-11-10 21:04:24 | 
{51374D2C-D96B-40F7-940B-6CB8E0A483A2} | TIMBER | WF | US-CA | Monterey | 25349.505227651814 | 100 | 2026-08-09 03:35:00 |  |  | 2026-11-17 16:16:58 | 
{C953057C-5469-4B86-AC90-D6D9DADA831F} | 0456 | WF | US-OR | Gilliam | 25252.8 | 100 | 2026-07-16 02:04:36 |  |  | 2026-11-10 17:14:35 | 
{532AE2EA-D27E-475B-A2A6-D4875FB9D8E7} | Snyder | WF | US-UT | Grand | 18122.942776754866 | 100 | 2026-06-27 05:10:19 |  |  | 2026-11-05 17:02:20 | 
{55C74279-0C6B-4CF7-BF16-731E6A8FB5F9} | McCully | WF | US-OR | Baker | 13604.184621187862 | 91 | 2026-08-22 21:28:00 |  |  | 2026-11-13 00:41:49 | 
{49D1FB0B-74D1-4A95-B8DF-066DCC5F06E1} | AUSTIN | WF | US-OR | Clackamas | 12888.016859658279 | 98 | 2026-08-09 17:12:59 |  |  | 2026-11-14 01:31:46 | 
{801A448C-B5B4-4DCC-BAE2-CEF8FEDBB2A6} | Bobcat Lakes | WF | US-MT | Beaverhead | 10895.743901629106 | 100 | 2026-07-31 20:39:00 |  |  | 2026-11-04 16:20:38 | 
{CF6B7836-AC84-4CC3-8725-058927BB4052} | Camp Creek | WF | US-MT | Powell | 9658.048202865326 | 100 | 2026-08-21 22:48:00 |  |  | 2026-11-16 19:22:42 | 
{C8034780-D588-48DA-8BC9-C6CED34CD8DF} | Paradise | WF | US-OR | Wallowa | 9656.288213838254 | 92 | 2026-07-16 19:38:00 |  |  | 2026-11-13 00:35:54 | 
{DFA477F2-305C-49CA-B82E-2AF072AB55F8} | THREE QUEENS | WF | US-WA | Kittitas | 9584 | 95 | 2026-07-16 04:28:00 |  |  | 2026-11-16 15:57:58 | 
{C4138756-16B2-412F-B32B-4DB4520DE5BC} | Silvertip | WF | US-MT | Flathead | 7279.558122475896 | 100 | 2026-07-24 21:19:15 |  |  | 2026-11-16 19:22:33 | 
{548A8D28-1A04-48EE-9011-ABA023175D43} | Willow | WF | US-CO | Lake | 7258.591764402346 | 92 | 2026-06-28 21:27:00 |  |  | 2026-11-12 23:08:15 | 
{8C9CB7A0-936C-4A64-AAEF-67A10E597A66} | Moose Mountain | WF | US-ID | Clearwater | 5831.690188235985 | 90 | 2026-07-30 00:02:00 |  |  | 2026-11-05 18:21:43 | 
{B0396AC9-6C41-4BC3-A899-F309FC28BAAE} | North Cayuse | WF | US-OR | Umatilla | 4887.367823220937 | 97 | 2026-07-04 22:01:00 |  |  | 2026-11-10 17:21:23 | 
{019119DA-16C0-40AE-ADFE-25AD80EA704E} | Slough Canyon | WF | US-UT | Grand | 4742.049184372984 | 100 | 2026-08-15 17:00:00 |  |  | 2026-11-09 16:57:14 | 
{DC4342D9-B479-44F1-906C-8ABD42E1F59C} | SISI | WF | US-WA | Chelan | 4687 | 90 | 2026-08-14 18:03:23 |  |  | 2026-11-10 03:07:03 | 
{E70E0FBE-8DD6-4E75-BCE8-8E5B9672A3C4} | KING | WF | US-WA | Kittitas | 3465 | 95 | 2026-08-19 23:09:24 |  |  | 2026-11-09 17:47:38 | 

### PULL 3

- Request 1 (page 0, resultOffset=0, resultRecordCount=1000): https://services3.arcgis.com/T4QMspbfLg3qTGWY/arcgis/rest/services/WFIGS_Interagency_Perimeters_Current/FeatureServer/0/query?where=1%3D1&outFields=*&returnGeometry=false&f=json&resultOffset=0&resultRecordCount=1000
- Requested at (UTC): 2026-11-19T05:40:16Z
- HTTP Date response header of the first request: Thu, 19 Nov 2026 05:40:18 GMT
- Status: 200. Features returned on the page: 53. exceededTransferLimit: absent — paging complete.
- Rows in wildfire-perimeters-pull3.csv: 53. SHA-256: 4b0e2b6ce62de260d60a1d042cc764999b10512dfecec1ef8defbcca7ae98aae
- Progress note on the platform record, recorded at 2026-11-19 05:41:11.012848+00 (Synmerco server time): "PULL 3: wildfire-perimeters-pull3.csv, 53 rows, SHA-256 4b0e2b6ce62de260d60a1d042cc764999b10512dfecec1ef8defbcca7ae98aae. First request 2026-11-19T05:40:16Z, HTTP Date Thu, 19 Nov 2026 05:40:18 GMT. Changes vs pull 2: new 9, gone 6, changed 8."

Top 20 wildfires of PULL 3, one fire per line, every kept field (key | incident name | type | state | county | gis acres | percent contained | discovered utc | contained utc | out utc | modified utc | flags), values as in the CSV:

{1CDF5E5A-F22E-4352-A582-C2A47663B93D} | Aspen Acres | WF | US-CO | Custer | 102003.46033741273 | 96 | 2026-06-29 12:04:46 |  |  | 2026-11-12 22:52:47 | 
{6AA4C355-AD18-472F-AAAB-78BAA9DE31B1} | GRASSHOPPER | WF | US-OR | Wasco | 93971.25018599666 | 98 | 2026-07-24 02:41:00 |  |  | 2026-11-14 01:29:56 | 
{D4E53810-46D0-48FB-889B-3E670328DCFB} | Hagen | WF | US-OR | Umatilla | 61379.583069531305 | 99 | 2026-07-16 23:20:00 |  |  | 2026-11-13 00:38:03 | 
{808808D2-F485-44FB-8819-F3C8C32138B8} | Wrights Spring | WF | US-OR | Klamath | 55134.464934912685 | 100 | 2026-08-05 21:56:00 |  |  | 2026-11-18 22:13:39 | 
{51374D2C-D96B-40F7-940B-6CB8E0A483A2} | TIMBER | WF | US-CA | Monterey | 25349.505227651814 | 100 | 2026-08-09 03:35:00 |  |  | 2026-11-17 16:16:58 | 
{532AE2EA-D27E-475B-A2A6-D4875FB9D8E7} | Snyder | WF | US-UT | Grand | 18122.942776754866 | 100 | 2026-06-27 05:10:19 |  |  | 2026-11-05 17:02:20 | 
{55C74279-0C6B-4CF7-BF16-731E6A8FB5F9} | McCully | WF | US-OR | Baker | 13604.184621187862 | 100 | 2026-08-22 21:28:00 |  |  | 2026-11-18 19:58:29 | 
{49D1FB0B-74D1-4A95-B8DF-066DCC5F06E1} | AUSTIN | WF | US-OR | Clackamas | 12888.016859658279 | 98 | 2026-08-09 17:12:59 |  |  | 2026-11-14 01:31:46 | 
{CF6B7836-AC84-4CC3-8725-058927BB4052} | Camp Creek | WF | US-MT | Powell | 9658.048202865326 | 100 | 2026-08-21 22:48:00 |  |  | 2026-11-16 19:22:42 | 
{C8034780-D588-48DA-8BC9-C6CED34CD8DF} | Paradise | WF | US-OR | Wallowa | 9656.288213838254 | 92 | 2026-07-16 19:38:00 |  |  | 2026-11-13 00:35:54 | 
{DFA477F2-305C-49CA-B82E-2AF072AB55F8} | THREE QUEENS | WF | US-WA | Kittitas | 9584 | 95 | 2026-07-16 04:28:00 |  |  | 2026-11-16 15:57:58 | 
{C4138756-16B2-412F-B32B-4DB4520DE5BC} | Silvertip | WF | US-MT | Flathead | 7279.558122475896 | 100 | 2026-07-24 21:19:15 |  |  | 2026-11-16 19:22:33 | 
{548A8D28-1A04-48EE-9011-ABA023175D43} | Willow | WF | US-CO | Lake | 7258.591764402346 | 92 | 2026-06-28 21:27:00 |  |  | 2026-11-12 23:08:15 | 
{8C9CB7A0-936C-4A64-AAEF-67A10E597A66} | Moose Mountain | WF | US-ID | Clearwater | 5831.690188235985 | 90 | 2026-07-30 00:02:00 |  |  | 2026-11-05 18:21:43 | 
{B0396AC9-6C41-4BC3-A899-F309FC28BAAE} | North Cayuse | WF | US-OR | Umatilla | 4887.367823220937 | 100 | 2026-07-04 22:01:00 |  |  | 2026-11-18 19:53:02 | 
{AA3DF707-B3F6-41B8-A5FF-BF502A918FFC} | Upper Smith | WF | US-ID | Boundary | 4848.046213986781 | 100 | 2026-07-08 15:29:00 |  |  | 2026-11-17 19:25:31 | 
{019119DA-16C0-40AE-ADFE-25AD80EA704E} | Slough Canyon | WF | US-UT | Grand | 4742.049184372984 | 100 | 2026-08-15 17:00:00 |  |  | 2026-11-09 16:57:14 | 
{DC4342D9-B479-44F1-906C-8ABD42E1F59C} | SISI | WF | US-WA | Chelan | 4687 | 90 | 2026-08-14 18:03:23 |  |  | 2026-11-10 03:07:03 | 
{E70E0FBE-8DD6-4E75-BCE8-8E5B9672A3C4} | KING | WF | US-WA | Kittitas | 3465 | 95 | 2026-08-19 23:09:24 |  |  | 2026-11-09 17:47:38 | 
{092F0D20-3543-4210-AB84-715E3714BA5F} | Signal Peak | WF | US-WA | Yakima | 3047.14 | 100 | 2026-07-24 22:57:04 |  |  | 2026-11-10 15:39:20 | 

## Data files

The three pull CSVs are attached as data files under Rule 25. One row per feature, never split; values as returned, times converted to UTC date and time; sorted by state, then key; key column key. Columns, in order: key, incident name, type, state, county, gis acres, percent contained, discovered utc, contained utc, out utc, modified utc, flags.

```synmerco-data
5940bf99869e7a8f3593f495544e8eadeabe7abd511235f27109dff734b3de1e wildfire-perimeters-pull1.csv
ca7855a0a6bfa850bc5a5dfbae0a0fca400b76d6c8ee1f9f556fc5adeb982850 wildfire-perimeters-pull2.csv
4b0e2b6ce62de260d60a1d042cc764999b10512dfecec1ef8defbcca7ae98aae wildfire-perimeters-pull3.csv
```
