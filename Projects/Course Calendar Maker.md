### Prompt:
Hello Gemini, I will paste HTML code containing my course schedule below this message.

Please perform the following:
1. Extract the weekly recurring course meetings (course name, days, start time, end time, location) and any listed single-event exams (course name, date, start time, end time, location). Please note the academic term if it's easily identifiable in the text (e.g., Spring 2025).
2. Generate the text content for an ICS file (`.ics`) containing these events.
3. **Important Formatting for ICS:** To ensure maximum compatibility and avoid previous import errors, please format the ICS data using these specific rules:
    * Use **floating times** for all `DTSTART` and `DTEND` properties (do not include `TZID=` or a `Z` suffix). The times should reflect the local times listed in the HTML.
    * Do **not** include a `VTIMEZONE` block in the file.
    * For recurring weekly events, use an `RRULE` property. Set the recurrence to end based on the last day of instruction for the identified academic term. You may need to ask me for the term/end date, or look up the standard academic calendar for the relevant institution/term if possible. The `UNTIL=` value should use the format `YYYYMMDDTHHMMSS` (local floating time).
    * Do **not** include any non-standard properties like color codes (`X-` properties).
4. Present the complete ICS text block, starting with `BEGIN:VCALENDAR` and ending with `END:VCALENDAR`, in your response so I can copy and save it directly as a `.ics` file (encoded as UTF-8).

Here is the HTML: