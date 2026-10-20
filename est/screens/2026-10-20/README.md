# EST · Bathroom — screens as shipped, 2026-10-20 (after EST-QA2)

The reference set for checking the estimate → contract flow, taken after Ivan's second round of fixes
(his comment of 19.10 on EST-QA1, https://trello.com/c/E6wE89oa). **This folder is the source for checks.**
No Miro frame for this set (decision of 20.10: without Miro for now).

- **Date:** 2026-10-20. Previous set: `../2026-10-19-qa1/`.
- **Code:** site `823869d` (tefcopro/site#19, EST-QA2: wizard, her pages and preview, the contractor's screens, no wraps), platform `38824d7` (tefcopro/platform#7, letter 2 label colours; no migration).
- **Where taken:** on the local stand built from these commits; no test orders were made in production (EST-DEL is not done yet). Letters come from Mailpit on that stand; their links point to the stand. All orders are new for this set.
- **Masked:** link tokens (`?k=…`) and one-time codes are replaced with `…` / `••••••` in letters and on the code screens (Development shows the code on screen).
- **Width:** `_390` — phone (390 px, @2x, fixed bars unpinned, full page); `_1440` — desktop. `11_her_confirm_sheet_390` and `13_decline_the_job_ask_390` are the visible viewport, as on a phone. The site footer is hidden in the page shots.
- **Letters:** colours are now kept. In the 19.10 sets the screenshot script masked 6-digit runs (codes) and also hit hex colours such as `#067647`, so greys and the green «Added» came out black there; the letters themselves were not affected.

## What changed since 2026-10-19-qa1 (EST-QA2)

- Wizard: one bottom bar and one «← Back» on every step; ZIP filled from the picked address (01); «View as Yulia sees it» everywhere (05); 03d — «Scope is complete» once, folded rows show the item and its answer; 04a error — the «Total 100%» plate neutral; «rough-in» not broken at the hyphen.
- No « · » left at a line end and no value split at 390: «About 22 working days», «Not included · 3» / «You take care of · 4», «How we check the work» / «3 inspections, 3 check-ins», «Signed and sent / waiting for Yulia», the link rows «Edit terms · Versions · Decline the job».
- «View as Yulia sees it»: ← Back, the Preview note, «From Azimuth X LLC · (704) 555-0142», then «Bathroom». Checked: no `?k=` in any link of the preview; «Download PDF» and «Version 1» go through the contractor's sign-in.
- Her pages: 08 Declined has the steps bar; 16 — the deposit block fills the card at 1440, «Copy» beside its value at 390.
- Contractor: 09 «The price assumes · 3 systems, 3 allowances»; 09 and 09b have the «My projects» tab and the avatar; 13a «Edit terms» a grey link without «›»; 16 — «Deposit $8,500 · waiting for Yulia» until it is received.
- Letter 2: «Added» green, «Now yours» blue, as on 09b / 10.

## Reference order

Bathroom · tub-to-shower conversion · Yulia Kolesnik, yulia.k@example.com, (704) 555-0199 · 2013 Autumn Blossom Ln, Waxhaw, NC 28173 · 3 photos before · contractor Azimuth X LLC (Dmitry Myslivets). Order T-261020-754D23.

- Version 1: $17,500 · start week of Nov 2 · about 21 working days · 50 / 40 / 10 → $8,750 / $7,000 / $1,750 · contractor pulls the permit · lights and fan bought by Yulia · allowances tile $900, vanity & top $1,800, faucets & trim $1,200.
- After the call, version 2: $17,000 · start week of Nov 16 · 22 working days · 50 / 35 / 15 → $8,500 / $5,950 / $2,550 · shower bench added, Yulia paints, Yulia orders the glass door.
- Yulia confirms v2 → contractor signs (code) → Yulia signs (code) → Active · deposit due.
- State orders (same homeowner and address, v1 terms, 3 photos): withdrawn T-261020-D8646B; expired (Valid until moved into the past on the stand) and then «Ask for current terms» T-261020-B6423C; confirmed and then declined by the contractor T-261020-611919; phone-only contact change T-261020-706DD4. `03d_settle`, `04_price` and `04a_*` are taken on a separate draft with the same terms.

## Files

| File | What |
|---|---|
| `01_new_estimate_site_390` | 1 · New estimate: site and homeowner |
| `02_kind_of_work_390` | 2 · Kind of work |
| `03a_variant_390` | 3a · Variant (six) |
| `03b_scope_work_390` | 3b · Work by stage, rows folded |
| `03c_scope_group_tile_390` | 3c · Group Tile open |
| `03c_scope_toilet_three_answers_390` | 3c · Toilet: three answers |
| `03c_scope_two_to_settle_390` | 3c · Work footer: 2 things to settle |
| `03d_settle_390` | 3d · N things to settle |
| `03d_scope_complete_390` | 3d · After the answers: Scope is complete |
| `03e_assumes_allowance_open_390` | 3e · The price assumes: allowance open, $1,200 typed, applied at once (no Save) |
| `03e_price_assumes_390` | 3e · The price assumes: systems and allowances |
| `04_price_390` | 4 · Price: $17,500 · 50 / 40 / 10 |
| `04a_price_custom_split_390` | 4a · Custom split 45 / 40 / 15 |
| `04a_price_custom_error_390` | 4a · Custom split: final 5% with escrow (error) |
| `05_check_and_send_390` | 5 · Check and send (no «Text the link») |
| `06_sent_not_opened_390` | 6 · Sent: head «Yulia Kolesnik · address», no number, no «Copy link» |
| `06_sent_opened_390` | 6 · Sent: Yulia opened it |
| `06_sent_v2_390` | 6 · Terms $17,000 sent |
| `06_view_as_yulia_preview_390` | 6 · «View as Yulia sees it» from Sent: her page 1:1 (chip, head, steps, «From Azimuth X LLC · phone», «Questions or changes?») under the note «Preview — this is what Yulia sees» |
| `06_withdraw_ask_390` | 6 · Withdraw: the question (full page) |
| `06_withdrawn_390` | State **Withdrawn** · contractor |
| `06_expired_390` | State **Expired** · contractor |
| `06_expired_she_asked_for_current_terms_390` | Expired, Yulia asked for current terms · contractor |
| `08_her_estimate_390`, `08_her_estimate_1440` | 8 · Her estimate, main screen (state **Sent**) |
| `08a_her_whats_included_390` | 8a · What's included |
| `08b_her_price_assumes_390` | 8b · The price assumes |
| `08c_her_how_it_goes_390` | 8c · How it goes |
| `08_her_withdrawn_390` | State **Withdrawn** · Yulia |
| `08_her_expired_390` | State **Expired** · Yulia |
| `08_her_asked_for_current_terms_390` | Expired, after «Ask for current terms» · Yulia |
| `08_her_declined_390` | State **Declined** · Yulia |
| `09_edit_terms_unchanged_390` | 9 · Edit terms, nothing changed |
| `09_edit_terms_price_open_390` | 9 · Edit terms: Price open |
| `09_edit_terms_4_changed_390` | 9 · Edit terms: 4 things changed |
| `09a_change_the_work_390` | 9a · Change the work: 3 changes, Framing open with Shower bench `NEW` |
| `09_edit_terms_5_changed_390` | 9 · Edit terms: 5 things changed |
| `09b_review_and_send_390` | 9b · Review and send |
| `09_change_contact_open_390` | 9 · «Wrong email or phone for Yulia? Change it» open |
| `09_change_contact_phone_saved_390` | 9 · Phone-only change: «Saved.» (EST-E1) |
| `10_her_updated_terms_390` | 10 · Updated terms: was → now |
| `11_her_confirm_sheet_390` | 11 · Confirmation sheet (viewport) |
| `12_her_confirmed_390` | 12 · State **Confirmed** · Yulia |
| `13_sign_the_contract_confirmed_390` | 13 · State **Confirmed** · contractor: Sign the contract |
| `13_sign_code_390` | 13 · Contractor's signing code |
| `13a_contractor_signed_waiting_390` | 13a · State **Contractor signed** · waiting for Yulia |
| `13_decline_the_job_ask_390` | 13 · Decline the job: the question |
| `13_declined_contractor_390` | State **Declined** · contractor |
| `14_her_contract_to_sign_390` | 14 · State **Contractor signed** · Yulia: the contract, Sign |
| `15_her_sign_code_390` | 15 · Her signing code |
| `16_her_signed_both_active_390`, `_1440` | State **Signed by both** · Yulia: Active · deposit due |
| `16_contractor_signed_both_active_390`, `_1440` | State **Signed by both** · contractor |
| `17_contract_v2_signed_by_both_p1…p5` | Contract PDF, version 2, signed by both, pages 1–5 (p4: §19 Trade Engine For Contractors and Owners Corp.; p5: Notice of Cancellation) |
| `contract_v2_signed_by_both.pdf` | The contract PDF itself |
| `email_01_estimate_sent` | Letter 1 · version 1 sent · to Yulia |
| `email_02_updated_terms` | Letter 2 · version 2 sent · to Yulia |
| `email_03_she_confirmed` | Letter 3 · she confirmed · to contractor |
| `email_04_contractor_signed` | Letter 4 · contractor signed · to Yulia |
| `email_05_code_contractor`, `email_05_code_homeowner` | Letter 5 · signing code, both parties |
| `email_06a_signed_both_homeowner` | Letter 6a · signed by both · to Yulia |
| `email_06b_signed_both_contractor` | Letter 6b · signed by both · to contractor |
| `email_07_withdrawn` | Letter 7 · withdrawn · to Yulia |
| `email_08_declined` | Letter 8 · contractor can't take the job · to Yulia |
| `email_09_expired` | Letter 9 · estimate expired · to contractor |
| `email_10_she_asked_for_current_terms` | Letter 10 (N-60) · she asked for current terms · to contractor |

Letters 1–10: subjects without the order number, the signature line «TEFCO keeps the record. The deal is between the two of you.» in each.
