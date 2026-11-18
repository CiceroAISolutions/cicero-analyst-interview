# Call data review

Marlowe & Finch Family Law is a family law firm in Phoenix, Arizona. On
August 31 they started a pilot of our AI receptionist, Ava. Ava answers when
the office is closed and when staff do not pick up. She runs a new-client
intake, offers a paid Discovery Call, transfers to staff during business hours,
and writes a summary of each call into the firm's CRM.

The pilot is ending. The managing partner, Rebecca Marlowe, is deciding this
week whether to keep going with us. Her email:

> We need to decide whether to keep Ava after the pilot. Show me what she has
> actually done for us since we went live. I have fifteen minutes between
> hearings. Don't send me a spreadsheet.

You just got this email, and your meeting with her is in 40 minutes. Your job
is to make the case for continuing: the impact and benefits we have created
since going live. Rebecca knows her own firm and will
question your numbers, so make a case that holds up.

All data here is made up. The firm, staff, and callers are fictional.

## What to do

1. **40 minutes.** Analyze the data. Use any LLM and any tools you like. Keep
   your screen shared.
2. **15 minutes.** Present your case to Rebecca. We play her. She is smart,
   busy, and not technical.
3. **15 minutes.** Talk with us about how you would turn this into a repeatable
   process.

What you present, and in what format, is up to you. A few points you can stand
behind are worth more than covering everything.

You can ask us questions at any point, the way you would ask a colleague or
the client.

## Files

Call data from our side. This is a simplified sample made for this exercise:

- `data/cicero.db` — the sample tables as one SQLite file
- `data/cicero/` — the same tables as CSV files, if you prefer those

| Table | What it holds |
|---|---|
| `cases` | One row per call: Ava's calls and the staff lines. Transcript, raw call data, CRM push status. |
| `data_sources` | Which kind of call a row is |
| `case_analysis` | Our summary and follow-up actions for each call |
| `case_enhanced_analysis` | Our labels for each call: category, how it ended, transfers, qualification |
| `case_status` | The status staff set for the call in our dashboard |
| `case_push_events` | Every attempt to write a call into the firm's CRM |
| `sent_messages` | Texts we sent to callers |
| `case_appointments` | Appointments Ava booked |
| `transcription_lines` | The staff members' recorded lines |
| `law_firms` | The firm's settings |

The firm's side:

- `data/crm/contacts.csv` and `data/crm/deals.csv` — one deal per potential
  new client, with its current stage, consultation, and retainer fields
- `data/crm/deal_stage_history.csv` — every stage change and what made it
- `data/crm/engagements.csv` — calls, notes, tasks, and meetings logged on
  contacts and deals
- `data/crm/owners.csv` — the firm's CRM users
- `data/callrail_calls.csv` — the firm's call-tracking log for its ad numbers

There is no data dictionary. Look at the data, and ask us when something is
unclear.

## Firm facts

- The firm's fees: Discovery Call $150, Consultation $350, Case Strategy
  Session $1,500. A client hires the firm by signing and paying a retainer.
- The pilot costs the firm $1,500 a month.
- Our own team tests the lines from `+16025550100` and `+16025550101`.
