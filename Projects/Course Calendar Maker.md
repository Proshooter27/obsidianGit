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
<body>
<header class="uw-header">
  <nav class="navbar">
    <div class="container-fluid">
      <div class="header-branding">
        <a class="navbar-brand" href="https://www.wisc.edu/" rel="noopener noreferrer" target="_blank" data-bcup-haslogintext="no">
          <img src="/courses-schedule/images/uw-crest-007b421a2f89bfb2738bf51f59d9ce1d.svg" width="40" height="62" class="uw-crest-svg d-inline-block" alt="UW logo, link to wisc.edu">
          <span id="title" class="fs-3 align-middle">
            Course Schedule
          </span>
        </a>
      </div>

      <ul class="nav nav-underline header-nav">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="/courses-schedule/" data-bcup-haslogintext="no">Course Schedule Calendar</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/courses-schedule/history" data-bcup-haslogintext="no">Course History &amp; Materials</a>
        </li>
      </ul>

      

      <div id="header-buttons" class="d-flex">
        <div id="header-help" class="dropstart">
          <button class="btn fs-3" style="color: var(--white);" data-bs-toggle="dropdown" data-bs-auto-close="true" aria-expanded="false" type="button" data-bcup-haslogintext="no">
            <i class="bi-question-circle-fill fs-3"></i>
          </button>
          <ul id="header-help-menu" class="dropdown-menu">
            <li><a class="dropdown-item link-primary" href="https://it.wisc.edu/services/help-desk/" data-bcup-haslogintext="no">Support</a></li>
            <li><a class="dropdown-item link-primary" href="https://enroll.wisc.edu/search" data-bcup-haslogintext="no">Course Search &amp; Enroll</a></li>
          </ul>
        </div>

        <div id="profile-wrapper" class="dropstart">
          <button id="profile-circle" type="button" class="btn btn-secondary-outline fs-3" data-bs-toggle="dropdown" data-bs-auto-close="true" aria-label="Profile menu" aria-controls="profile-nav" aria-haspopup="true" aria-expanded="false" data-bcup-haslogintext="no">
            <p id="profile-circle-initial">
              O
            </p>
          </button>
          <ul id="profile-nav" class="dropdown-menu" aria-labelledby="profile-circle" role="menu" tabindex="-1">
            <p id="profile-nav-user" class="dropdown-item">Ojas Patil</p>
            <li><a class="dropdown-item" href="/Shibboleth.sso/Logout?return=https://login.wisc.edu/logout" data-bcup-haslogintext="no">Logout</a></li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</header>



<main class="container">
  <section id="schedule-tab-container">
    <section class="mt-3">
    <div class="notes mt-3">
        <h2>Course Schedule Calendar</h2>
        <p class="fs-6 fw-light">Details for courses and sections are available beneath table, and clicking on an event in the table will direct you to details</p>
        <p class="fs-6 fw-light">
            To access your Canvas Courses and training(s) in Canvas go to your
            <a href="https://canvas.wisc.edu/" target="_blank" data-bcup-haslogintext="no">Canvas Dashboard</a>.
        </p>
        <p class="fs-6 fw-lighter">
            All listed times are in the US Central time zone
        </p>
    </div>

    <form id="term-select" action="/courses-schedule/" method="get">
        <label for="term-code">Select Term:</label>
        <div class="input-group">
            <select id="term-code" name="termCode" class="form-select mb-2" aria-label="Select term">
                <option value="1254" selected="selected">Spring 2025</option>
                <option value="1256">Summer 2025</option>
                <option value="1262">Fall 2025</option>
            </select>
            <div>
                <button type="submit" class="btn btn-primary" data-bcup-haslogintext="no">
                    <span class="spinner-border spinner-border-sm d-none invisible" aria-hidden="true"></span>
                    <span role="status" class="d-inline-block">Update</span>
                </button>
            </div>
        </div>
        <input id="term-select-uid" name="searchNetId" type="hidden">
    </form>

    <div id="calendar" class="fc fc-media-screen fc-direction-ltr fc-theme-standard"><div class="fc-header-toolbar fc-toolbar fc-toolbar-ltr"><div class="fc-toolbar-chunk"></div><div class="fc-toolbar-chunk"></div><div class="fc-toolbar-chunk"></div></div><div aria-labelledby="fc-dom-1" class="fc-view-harness fc-view-harness-passive"><div class="fc-timeGridWeek-view fc-view fc-timegrid"><table role="grid" class="fc-scrollgrid "><thead role="rowgroup"><tr role="presentation" class="fc-scrollgrid-section fc-scrollgrid-section-header  fc-scrollgrid-section-sticky"><th role="presentation"><div class="fc-scroller-harness"><div class="fc-scroller" style="overflow: visible;"><table role="presentation" class="fc-col-header " style="width: 1294px;"><colgroup><col style="width: 50px;"></colgroup><thead role="presentation"><tr role="row"><th aria-hidden="true" class="fc-timegrid-axis"><div class="fc-timegrid-axis-frame"></div></th><th role="columnheader" data-date="2023-01-01" class="fc-col-header-cell fc-day fc-day-sun fc-day-past"><div class="fc-scrollgrid-sync-inner"><a aria-label="Sunday" class="fc-col-header-cell-cushion" data-bcup-haslogintext="no">Sun</a></div></th><th role="columnheader" data-date="2023-01-02" class="fc-col-header-cell fc-day fc-day-mon fc-day-past"><div class="fc-scrollgrid-sync-inner"><a aria-label="Monday" class="fc-col-header-cell-cushion" data-bcup-haslogintext="no">Mon</a></div></th><th role="columnheader" data-date="2023-01-03" class="fc-col-header-cell fc-day fc-day-tue fc-day-past"><div class="fc-scrollgrid-sync-inner"><a aria-label="Tuesday" class="fc-col-header-cell-cushion" data-bcup-haslogintext="no">Tue</a></div></th><th role="columnheader" data-date="2023-01-04" class="fc-col-header-cell fc-day fc-day-wed fc-day-past"><div class="fc-scrollgrid-sync-inner"><a aria-label="Wednesday" class="fc-col-header-cell-cushion" data-bcup-haslogintext="no">Wed</a></div></th><th role="columnheader" data-date="2023-01-05" class="fc-col-header-cell fc-day fc-day-thu fc-day-past"><div class="fc-scrollgrid-sync-inner"><a aria-label="Thursday" class="fc-col-header-cell-cushion" data-bcup-haslogintext="no">Thu</a></div></th><th role="columnheader" data-date="2023-01-06" class="fc-col-header-cell fc-day fc-day-fri fc-day-past"><div class="fc-scrollgrid-sync-inner"><a aria-label="Friday" class="fc-col-header-cell-cushion" data-bcup-haslogintext="no">Fri</a></div></th><th role="columnheader" data-date="2023-01-07" class="fc-col-header-cell fc-day fc-day-sat fc-day-past"><div class="fc-scrollgrid-sync-inner"><a aria-label="Saturday" class="fc-col-header-cell-cushion" data-bcup-haslogintext="no">Sat</a></div></th></tr></thead></table></div></div></th></tr></thead><tbody role="rowgroup"><tr role="presentation" class="fc-scrollgrid-section fc-scrollgrid-section-body "><td role="presentation"><div class="fc-scroller-harness"><div class="fc-scroller" style="overflow: visible;"><div class="fc-timegrid-body" style="width: 1294px;"><div class="fc-timegrid-slots"><table aria-hidden="true" class="" style="width: 1294px; height: 599px;"><colgroup><col style="width: 50px;"></colgroup><tbody><tr><td data-time="11:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">11am</div></div></td><td data-time="11:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="11:30:00"></td><td data-time="11:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="12:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">12pm</div></div></td><td data-time="12:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="12:30:00"></td><td data-time="12:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="13:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">1pm</div></div></td><td data-time="13:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="13:30:00"></td><td data-time="13:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="14:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">2pm</div></div></td><td data-time="14:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="14:30:00"></td><td data-time="14:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="15:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">3pm</div></div></td><td data-time="15:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="15:30:00"></td><td data-time="15:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="16:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">4pm</div></div></td><td data-time="16:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="16:30:00"></td><td data-time="16:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="17:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">5pm</div></div></td><td data-time="17:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="17:30:00"></td><td data-time="17:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="18:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">6pm</div></div></td><td data-time="18:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="18:30:00"></td><td data-time="18:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="19:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">7pm</div></div></td><td data-time="19:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="19:30:00"></td><td data-time="19:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="20:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">8pm</div></div></td><td data-time="20:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="20:30:00"></td><td data-time="20:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="21:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">9pm</div></div></td><td data-time="21:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="21:30:00"></td><td data-time="21:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr><tr><td data-time="22:00:00" class="fc-timegrid-slot fc-timegrid-slot-label fc-scrollgrid-shrink"><div class="fc-timegrid-slot-label-frame fc-scrollgrid-shrink-frame"><div class="fc-timegrid-slot-label-cushion fc-scrollgrid-shrink-cushion">10pm</div></div></td><td data-time="22:00:00" class="fc-timegrid-slot fc-timegrid-slot-lane"></td></tr><tr><td class="fc-timegrid-slot fc-timegrid-slot-label fc-timegrid-slot-minor" data-time="22:30:00"></td><td data-time="22:30:00" class="fc-timegrid-slot fc-timegrid-slot-lane fc-timegrid-slot-minor"></td></tr></tbody></table></div><div class="fc-timegrid-cols"><table role="presentation" style="width: 1294px;"><colgroup><col style="width: 50px;"></colgroup><tbody role="presentation"><tr role="row"><td aria-hidden="true" class="fc-timegrid-col fc-timegrid-axis"><div class="fc-timegrid-col-frame"><div class="fc-timegrid-now-indicator-container"></div></div></td><td role="gridcell" data-date="2023-01-01" class="fc-day fc-day-sun fc-day-past fc-timegrid-col"><div class="fc-timegrid-col-frame"><div class="fc-timegrid-col-bg"></div><div class="fc-timegrid-col-events"></div><div class="fc-timegrid-col-events"></div><div class="fc-timegrid-now-indicator-container"></div></div></td><td role="gridcell" data-date="2023-01-02" class="fc-day fc-day-mon fc-day-past fc-timegrid-col"><div class="fc-timegrid-col-frame"><div class="fc-timegrid-col-bg"></div><div class="fc-timegrid-col-events"><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 0px 0% -41px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(0, 136, 23);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">11:00am - 11:50am</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">MATH 234 LEC 003</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 170px 0% -212px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(74, 119, 180);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">2:25pm - 3:15pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">E C E 352 LEC 002</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 225px 0% -320px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(19, 63, 216);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">3:30pm - 5:25pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">E C E 210 LAB 302</div></div></div></div></a></div></div><div class="fc-timegrid-col-events"></div><div class="fc-timegrid-now-indicator-container"></div></div></td><td role="gridcell" data-date="2023-01-03" class="fc-day fc-day-tue fc-day-past fc-timegrid-col"><div class="fc-timegrid-col-frame"><div class="fc-timegrid-col-bg"></div><div class="fc-timegrid-col-events"><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 100px 0% -162px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(134, 0, 0);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">1:00pm - 2:15pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">ENGL 100 LEC 063</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 170px 0% -212px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(87, 76, 250);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">2:25pm - 3:15pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">PHYSICS 201 LEC 002</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 225px 0% -266px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(0, 136, 23);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">3:30pm - 4:20pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">MATH 234 DIS 352</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 279px 0% -320px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(87, 76, 250);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">4:35pm - 5:25pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">PHYSICS 201 DIS 316</div></div></div></div></a></div></div><div class="fc-timegrid-col-events"></div><div class="fc-timegrid-now-indicator-container"></div></div></td><td role="gridcell" data-date="2023-01-04" class="fc-day fc-day-wed fc-day-past fc-timegrid-col"><div class="fc-timegrid-col-frame"><div class="fc-timegrid-col-bg"></div><div class="fc-timegrid-col-events"><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 0px 0% -41px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(0, 136, 23);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">11:00am - 11:50am</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">MATH 234 LEC 003</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 170px 0% -212px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(74, 119, 180);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">2:25pm - 3:15pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">E C E 352 LEC 002</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 225px 0% -325px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(74, 119, 180);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">3:30pm - 5:30pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">E C E 352 LAB 303</div></div></div></div></a></div></div><div class="fc-timegrid-col-events"></div><div class="fc-timegrid-now-indicator-container"></div></div></td><td role="gridcell" data-date="2023-01-05" class="fc-day fc-day-thu fc-day-past fc-timegrid-col"><div class="fc-timegrid-col-frame"><div class="fc-timegrid-col-bg"></div><div class="fc-timegrid-col-events"><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 100px 0% -162px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(134, 0, 0);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">1:00pm - 2:15pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">ENGL 100 LEC 063</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 170px 0% -212px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(87, 76, 250);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">2:25pm - 3:15pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">PHYSICS 201 LEC 002</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 225px 0% -266px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(0, 136, 23);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">3:30pm - 4:20pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">MATH 234 DIS 352</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 279px 0% -320px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(87, 76, 250);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">4:35pm - 5:25pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">PHYSICS 201 DIS 316</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 404px 0% -550px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(87, 76, 250);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">7:05pm - 10:00pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">PHYSICS 201 LAB 616</div></div></div></div></a></div></div><div class="fc-timegrid-col-events"></div><div class="fc-timegrid-now-indicator-container"></div></div></td><td role="gridcell" data-date="2023-01-06" class="fc-day fc-day-fri fc-day-past fc-timegrid-col"><div class="fc-timegrid-col-frame"><div class="fc-timegrid-col-bg"></div><div class="fc-timegrid-col-events"><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 0px 0% -41px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(0, 136, 23);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">11:00am - 11:50am</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">MATH 234 LEC 003</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 54px 0% -95px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(19, 63, 216);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">12:05pm - 12:55pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">E C E 210 LEC 001</div></div></div></div></a></div><div class="fc-timegrid-event-harness fc-timegrid-event-harness-inset" style="inset: 170px 0% -212px; z-index: 1;"><a tabindex="0" class="fc-event fc-event-start fc-event-end fc-event-past fc-timegrid-event fc-v-event" style="background-color: rgb(74, 119, 180);" data-bcup-haslogintext="no"><div class="fc-event-main"><div class="fc-event-main-frame"><div class="fc-event-time">2:25pm - 3:15pm</div><div class="fc-event-title-container"><div class="fc-event-title fc-sticky">E C E 352 LEC 002</div></div></div></div></a></div></div><div class="fc-timegrid-col-events"></div><div class="fc-timegrid-now-indicator-container"></div></div></td><td role="gridcell" data-date="2023-01-07" class="fc-day fc-day-sat fc-day-past fc-timegrid-col"><div class="fc-timegrid-col-frame"><div class="fc-timegrid-col-bg"></div><div class="fc-timegrid-col-events"></div><div class="fc-timegrid-col-events"></div><div class="fc-timegrid-now-indicator-container"></div></div></td></tr></tbody></table></div></div></div></div></td></tr></tbody></table></div></div></div>

    <section id="courses-list" class="mt-4 mb-4">
        <h3 class="fs-2">Courses</h3>

        

        <div id="course-meetings" class="mt-4">
            
  
    <strong class="fs-3">E C E 352: Digital System Fundamentals</strong>
    <br>
    <strong>Weekly Meetings</strong>
    <ul>
      
        
          <li>
            <strong id="79102">LEC 002</strong>

            <span>
                        M
                        2:25 PM
                      - 3:15 PM
                        Engineering Hall Room 2255
                      </span>

            
          </li>
        
      
        
          <li>
            <strong id="62478">LAB 303</strong>

            <span>
                        W
                        3:30 PM
                      - 5:30 PM
                        Engineering Hall Room 3654
                      </span>

            
          </li>
        
      
    </ul>
  

  <strong>Exams</strong>
  
  <ul>
    <li>
      <span>
             May 9, 5:05 PM
           - 7:05 PM
           - Location not specified
           </span>
    </li>
  </ul>

        </div>

        <div id="course-meetings" class="mt-4">
            
  
    <strong class="fs-3">E C E 210: Introductory Experience in Electrical Engineering</strong>
    <br>
    <strong>Weekly Meetings</strong>
    <ul>
      
        
          <li>
            <strong id="76323">LEC 001</strong>

            <span>
                        F
                        12:05 PM
                      - 12:55 PM
                        Wendt Commons Room 311
                      </span>

            
          </li>
        
      
        
          <li>
            <strong id="76326">LAB 302</strong>

            <span>
                        M
                        3:30 PM
                      - 5:25 PM
                        Engineering Hall Room 1438
                      </span>

            <ul>
              <li>
                <em>The requisite "Pre-progression engineering students, all ECE students, AMEP students, or junior BME students" will be lifted on Jan 17th, 2025.</em>
              </li>
            </ul>
          </li>
        
      
    </ul>
  

  <strong>Exams</strong>
  <ul>
    <li><em>None provided</em></li>
  </ul>
  <ul>
    
  </ul>

        </div>

        <div id="course-meetings" class="mt-4">
            
  
    <strong class="fs-3">ENGL 100: Introduction to College Composition</strong>
    <br>
    <strong>Weekly Meetings</strong>
    <ul>
      
        
          <li>
            <strong id="81185">LEC 063</strong>

            <span>
                        TR
                        1:00 PM
                      - 2:15 PM
                        Van Hise Hall Room 579
                      </span>

            
          </li>
        
      
    </ul>
  

  <strong>Exams</strong>
  <ul>
    <li><em>None provided</em></li>
  </ul>
  <ul>
    
  </ul>

        </div>

        <div id="course-meetings" class="mt-4">
            
  
    <strong class="fs-3">INTER-LS 145: How to Succeed in College</strong>
    <br>
    <strong>Weekly Meetings</strong>
    <ul>
      
        
          <li>
            <strong id="73662">LEC 001</strong>

            <span>
                        
                        
                      - 
                        ONLINE
                      </span>

            
          </li>
        
      
    </ul>
  

  <strong>Exams</strong>
  <ul>
    <li><em>None provided</em></li>
  </ul>
  <ul>
    
  </ul>

        </div>

        <div id="course-meetings" class="mt-4">
            
  
    <strong class="fs-3">MATH 234: Calculus--Functions of Several Variables</strong>
    <br>
    <strong>Weekly Meetings</strong>
    <ul>
      
        
          <li>
            <strong id="63509">LEC 003</strong>

            <span>
                        MWF
                        11:00 AM
                      - 11:50 AM
                        Van Vleck Hall Room B102
                      </span>

            <ul>
              <li>
                <em>This course may have evening midterm exams. Please consult the syllabus for precise information.</em>
              </li>
            </ul>
          </li>
        
      
        
          <li>
            <strong id="84585">DIS 352</strong>

            <span>
                        TR
                        3:30 PM
                      - 4:20 PM
                        Van Vleck Hall Room B329
                      </span>

            
          </li>
        
      
    </ul>
  

  <strong>Exams</strong>
  
  <ul>
    <li>
      <span>
             May 7, 2:45 PM
           - 4:45 PM
           - Sterling Hall Room 1310
           </span>
    </li>
  </ul>

        </div>

        <div id="course-meetings" class="mt-4">
            
  
    <strong class="fs-3">PHYSICS 201: General Physics</strong>
    <br>
    <strong>Weekly Meetings</strong>
    <ul>
      
        
          <li>
            <strong id="74118">LEC 002</strong>

            <span>
                        TR
                        2:25 PM
                      - 3:15 PM
                        Chamberlin Hall Room 2103
                      </span>

            
          </li>
        
      
        
          <li>
            <strong id="74174">DIS 316</strong>

            <span>
                        TR
                        4:35 PM
                      - 5:25 PM
                        Sterling Hall Room 2319
                      </span>

            
          </li>
        
      
        
          <li>
            <strong id="74171">LAB 616</strong>

            <span>
                        R
                        7:05 PM
                      - 10:00 PM
                        Chamberlin Hall Room 4314
                      </span>

            
          </li>
        
      
    </ul>
  

  <strong>Exams</strong>
  
  <ul>
    <li>
      <span>
             May 9, 5:05 PM
           - 7:05 PM
           - Ingraham Hall Room B10
           </span>
    </li>
  </ul>

        </div>
    </section>
</section>
  </section>
</main>

<footer class="d-flex justify-content-center fw-lighter">
  <ul>
    <li class="d-flex"><a href="/courses-schedule/accessibility" data-bcup-haslogintext="no"><p>Accessibility Statement</p></a></li>
    
    <li class="metadata">Version: 1.0.6</li>
  </ul>
</footer>


<div id="bettercanvas-reminders" style="display: flex;"><div class="bettercanvas-reminder-wrapper"><div class="bettercanvas-reminder-container"><div><svg xmlns="http://www.w3.org/2000/svg" fill="#ff4545" width="25px" height="25px" viewBox="-192 -192 2304.00 2304.00" stroke="white"><g stroke-width="0"><rect x="-192" y="-192" width="2304.00" height="2304.00" rx="0" fill="none" strokewidth="0"></rect></g><g stroke-linecap="round" stroke-linejoin="round"></g><g> <path d="M958.568 277.97C1100.42 277.97 1216.48 171.94 1233.67 34.3881 1146.27 12.8955 1054.57 0 958.568 0 864.001 0 770.867 12.8955 683.464 34.3881 700.658 171.94 816.718 277.97 958.568 277.97ZM35.8207 682.031C173.373 699.225 279.403 815.285 279.403 957.136 279.403 1098.99 173.373 1215.05 35.8207 1232.24 12.8953 1144.84 1.43262 1051.7 1.43262 957.136 1.43262 862.569 12.8953 769.434 35.8207 682.031ZM528.713 957.142C528.713 1005.41 489.581 1044.55 441.31 1044.55 393.038 1044.55 353.907 1005.41 353.907 957.142 353.907 908.871 393.038 869.74 441.31 869.74 489.581 869.74 528.713 908.871 528.713 957.142ZM1642.03 957.136C1642.03 1098.99 1748.06 1215.05 1885.61 1232.24 1908.54 1144.84 1920 1051.7 1920 957.136 1920 862.569 1908.54 769.434 1885.61 682.031 1748.06 699.225 1642.03 815.285 1642.03 957.136ZM1567.51 957.142C1567.51 1005.41 1528.38 1044.55 1480.11 1044.55 1431.84 1044.55 1392.71 1005.41 1392.71 957.142 1392.71 908.871 1431.84 869.74 1480.11 869.74 1528.38 869.74 1567.51 908.871 1567.51 957.142ZM958.568 1640.6C816.718 1640.6 700.658 1746.63 683.464 1884.18 770.867 1907.11 864.001 1918.57 958.568 1918.57 1053.14 1918.57 1146.27 1907.11 1233.67 1884.18 1216.48 1746.63 1100.42 1640.6 958.568 1640.6ZM1045.98 1480.11C1045.98 1528.38 1006.85 1567.51 958.575 1567.51 910.304 1567.51 871.172 1528.38 871.172 1480.11 871.172 1431.84 910.304 1392.71 958.575 1392.71 1006.85 1392.71 1045.98 1431.84 1045.98 1480.11ZM1045.98 439.877C1045.98 488.148 1006.85 527.28 958.575 527.28 910.304 527.28 871.172 488.148 871.172 439.877 871.172 391.606 910.304 352.474 958.575 352.474 1006.85 352.474 1045.98 391.606 1045.98 439.877ZM1441.44 1439.99C1341.15 1540.29 1333.98 1697.91 1418.52 1806.8 1579 1712.23 1713.68 1577.55 1806.82 1418.5 1699.35 1332.53 1541.74 1339.7 1441.44 1439.99ZM1414.21 1325.37C1414.21 1373.64 1375.08 1412.77 1326.8 1412.77 1278.53 1412.77 1239.4 1373.64 1239.4 1325.37 1239.4 1277.1 1278.53 1237.97 1326.8 1237.97 1375.08 1237.97 1414.21 1277.1 1414.21 1325.37ZM478.577 477.145C578.875 376.846 586.039 219.234 501.502 110.339 341.024 204.906 206.338 339.592 113.203 498.637 220.666 584.607 378.278 576.01 478.577 477.145ZM679.155 590.32C679.155 638.591 640.024 677.723 591.752 677.723 543.481 677.723 504.349 638.591 504.349 590.32 504.349 542.048 543.481 502.917 591.752 502.917 640.024 502.917 679.155 542.048 679.155 590.32ZM1440 475.712C1540.3 576.01 1697.91 583.174 1806.8 498.637 1712.24 338.159 1577.55 203.473 1418.51 110.339 1332.54 217.801 1341.13 375.413 1440 475.712ZM1414.21 590.32C1414.21 638.591 1375.08 677.723 1326.8 677.723 1278.53 677.723 1239.4 638.591 1239.4 590.32 1239.4 542.048 1278.53 502.917 1326.8 502.917 1375.08 502.917 1414.21 542.048 1414.21 590.32ZM477.145 1438.58C376.846 1338.28 219.234 1331.12 110.339 1415.65 204.906 1576.13 339.593 1710.82 498.637 1805.39 584.607 1696.49 577.443 1538.88 477.145 1438.58ZM679.155 1325.37C679.155 1373.64 640.024 1412.77 591.752 1412.77 543.481 1412.77 504.349 1373.64 504.349 1325.37 504.349 1277.1 543.481 1237.97 591.752 1237.97 640.024 1237.97 679.155 1277.1 679.155 1325.37Z"></path></g></svg></div><a class="bettercanvas-reminder-content" href="https://canvas.wisc.edu/courses/438168/assignments/2612599" target="_blank" data-bcup-haslogintext="no"><h2 class="bettercanvas-reminder-title">Short Assignment #4: Revision w/Risk</h2><p class="bettercanvas-reminder-due">Assignment due in 1 hour</p></a></div><btn class="bettercanvas-reminder-hide">x</btn></div></div></body>