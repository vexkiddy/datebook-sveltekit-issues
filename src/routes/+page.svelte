<script>
    import {ICalendar, GoogleCalendar, OutlookCalendar, YahooCalendar} from "datebook";
    
    const CalendarOptions = {
        title: "Test Event",
        location: "Stone Henge",
        start: new Date("01/01/2023"),
        end: new Date("06/01/2023")
    }
    
    const google = new GoogleCalendar(CalendarOptions)
    const outlook = new OutlookCalendar(CalendarOptions)
    const yahoo = new YahooCalendar(CalendarOptions)
    const ical = new ICalendar(CalendarOptions)



</script>


<button on:click={() => window.open(google.render(), "_blank")}>Google Calender</button>
<button on:click={() => window.open(outlook.render(), "_blank")}>Outlook Calender</button>
<button on:click={() => window.open(yahoo.render(), "_blank")}>Yahoo Calender</button>
<button on:click={() => ical.download()}>iCal</button>


