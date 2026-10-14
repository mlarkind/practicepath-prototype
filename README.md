Matthew Larkin
ESTM 60244, Current State and Future of Generative AI
Project First Working Slice
October 13, 2026

Note. Tests appear in the section titled Three test results. Known limitations appear in the section titled Known limitations.

PracticePath Prototype

PracticePath is a pipeline map that helps a physician or owner of an independent medical practice name one restorative reproductive medicine (RRM) seat and see a short list of sample residents or fellows who might fit.

What the first working slice allows a user to do
Enter one open doctor seat (specialty, methods, start window, and whether a funded training year is offered).
Click Show who might fit to see a short list of sample residents or fellows with a fit label and short rationale.
Accept or reject each suggestion.
Accepting places a visible hold on that person until the stated start window. Rejecting does nothing further.

Link to open the prototype
Open the prototype here https://lovable.dev/preview/yR619TRe8jP1bYPlAdgHA4mZY4PcY58H

On the page fill in the seat form and click Show who might fit to run the flow. Built in Lovable. No Replit was used.

Public GitHub repository
https://github.com/mlarkind/practicepath-prototype

AI role and transparency

What the future AI system is intended to do
The future AI system is intended to find residents and fellows who want to practice restorative reproductive medicine, place them on the practice pipeline map by stage and method, and produce a short list with a fit label and editable rationale. The practice keeps full control. The AI does not message anyone or create a hold.

Which behavior currently works
The user can enter one seat, receive a short list of sample profiles with fit labels and short rationales, and accept or reject each suggestion. Accepting places a visible hold. The flow is complete and understandable.

Which behavior is simulated or completed manually
Matching and rationales are fully simulated with prewritten sample data. No live AI model is connected. The results are recommendations only. The practice decides what to accept.

Three test results

| Test | Input or action | What happened | Pass, partial, or fail |
|------|-----------------|---------------|------------------------|
| Typical case | Specialty OB/GYN. Methods Creighton. Start window July 2027. Funded training year Yes. Note High patient demand for Creighton trained care. Clicked Show who might fit. | Showed sample profiles. Top result Dr. Maria Alvarez (PGY 3 OB/GYN Creighton NaPro) labeled Strong fit with rationale about shared Creighton, July 2027 availability, and funding. Other results Partial. Simulated note visible. Accept and Reject buttons shown. | Pass |
| Challenge case | Specialty Endocrinology. Methods Marquette. Start window 2028. Funded training year No. Note maybe some interest in methods. Clicked Show who might fit. | Returned three Partial results only. Rationales noted mismatches in specialty, methods, timing, or funding needs. No Strong fit. Simulated note visible. | Pass |
| Invalid or empty case | Methods left unchecked. Note left empty. Defaults kept (OB/GYN, July 2027, Funded Yes). Clicked Show who might fit. | Still showed results. Dr. Maria Alvarez labeled Strong fit but rationale said no shared methods. Other profiles also noted no shared methods. No clear error or empty state message. | Partial |

Known limitations
Medical residents and fellows shown are example profiles only. Matching and rationales are simulated with sample data.
No data is saved. Refreshing the page clears the seat and any holds.
A way to show actual med residents instead of example profiles was intentionally left outside this first slice.
