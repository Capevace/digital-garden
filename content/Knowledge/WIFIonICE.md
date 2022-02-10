# WIFIonICE – Reverse Engineered

\#reverseengineered #dev #interesting

## Train status

````http
GET https://iceportal.de/api1/rs/status
````

````json
{
  "connection": true,
  "serviceLevel": "AVAILABLE_SERVICE",
  "gpsStatus": "VALID",
  "internet": "HIGH",
  "latitude": 52.28249666666667,
  "longitude": 8.993446666666667,
  "tileY": 253,
  "tileX": -44,
  "series": "807",
  "serverTime": 1637308797778,
  "speed": 135,
  "trainType": "ICE",
  "tzn": "Tz225",
  "wagonClass": "SECOND",
  "connectivity": {
    "currentState": "HIGH",
    "nextState": "UNSTABLE",
    "remainingTimeSeconds": 9000
  },
  "bapInstalled": true
}
````

*📝    ToDo*

## Trip Info

````http
GET https://iceportal.de/api1/rs/tripInfo/trip
````

````json
{
  "trip": {
    "tripDate": "2021-11-19",
    "trainType": "ICE",
    "vzn": "654",
    "actualPosition": 251316,
    "distanceFromLastStop": 37659,
    "totalDistance": 509964,
    "stopInfo": {
      "scheduledNext": "8000036_00",
      "actualNext": "8000036_00",
      "actualLast": "8000152_00",
      "actualLastStarted": "8000036",
      "finalStationName": "Köln Hbf",
      "finalStationEvaNr": "8000207_00"
    },
    "stops": [
      {
        "station": {
          "evaNr": "8010255_00",
          "name": "Berlin Ostbahnhof",
          "code": null,
          "geocoordinates": {
            "latitude": 52.510488,
            "longitude": 13.434681
          }
        },
        "timetable": {
          "scheduledArrivalTime": null,
          "actualArrivalTime": null,
          "showActualArrivalTime": null,
          "arrivalDelay": "",
          "scheduledDepartureTime": 1637300100000,
          "actualDepartureTime": 1637300100000,
          "showActualDepartureTime": true,
          "departureDelay": ""
        },
        "track": {
          "scheduled": "6",
          "actual": "6"
        },
        "info": {
          "status": 0,
          "passed": true,
          "positionStatus": "passed",
          "distance": 0,
          "distanceFromStart": 0
        },
        "delayReasons": null
      },
      {
        "station": {
          "evaNr": "8011160_00",
          "name": "Berlin Hbf",
          "code": null,
          "geocoordinates": {
            "latitude": 52.525592,
            "longitude": 13.369545
          }
        },
        "timetable": {
          "scheduledArrivalTime": 1637300520000,
          "actualArrivalTime": 1637300580000,
          "showActualArrivalTime": true,
          "arrivalDelay": "+1",
          "scheduledDepartureTime": 1637300760000,
          "actualDepartureTime": 1637300760000,
          "showActualDepartureTime": true,
          "departureDelay": ""
        },
        "track": {
          "scheduled": "13",
          "actual": "13"
        },
        "info": {
          "status": 0,
          "passed": true,
          "positionStatus": "passed",
          "distance": 4718,
          "distanceFromStart": 4718
        },
        "delayReasons": null
      },
      {
        "station": {
          "evaNr": "8010404_00",
          "name": "Berlin-Spandau",
          "code": null,
          "geocoordinates": {
            "latitude": 52.534648,
            "longitude": 13.196898
          }
        },
        "timetable": {
          "scheduledArrivalTime": 1637301600000,
          "actualArrivalTime": 1637301660000,
          "showActualArrivalTime": true,
          "arrivalDelay": "+1",
          "scheduledDepartureTime": 1637301720000,
          "actualDepartureTime": 1637301840000,
          "showActualDepartureTime": true,
          "departureDelay": "+2"
        },
        "track": {
          "scheduled": "4",
          "actual": "4"
        },
        "info": {
          "status": 0,
          "passed": true,
          "positionStatus": "passed",
          "distance": 11725,
          "distanceFromStart": 16443
        },
        "delayReasons": null
      },
      {
        "station": {
          "evaNr": "8006552_00",
          "name": "Wolfsburg Hbf",
          "code": null,
          "geocoordinates": {
            "latitude": 52.429498,
            "longitude": 10.787784
          }
        },
        "timetable": {
          "scheduledArrivalTime": 1637304720000,
          "actualArrivalTime": 1637304900000,
          "showActualArrivalTime": true,
          "arrivalDelay": "+3",
          "scheduledDepartureTime": 1637304780000,
          "actualDepartureTime": 1637305020000,
          "showActualDepartureTime": true,
          "departureDelay": "+4"
        },
        "track": {
          "scheduled": "1",
          "actual": "1"
        },
        "info": {
          "status": 0,
          "passed": true,
          "positionStatus": "passed",
          "distance": 163599,
          "distanceFromStart": 180042
        },
        "delayReasons": null
      },
      {
        "station": {
          "evaNr": "8000152_00",
          "name": "Hannover Hbf",
          "code": null,
          "geocoordinates": {
            "latitude": 52.376761,
            "longitude": 9.741021
          }
        },
        "timetable": {
          "scheduledArrivalTime": 1637306880000,
          "actualArrivalTime": 1637307000000,
          "showActualArrivalTime": true,
          "arrivalDelay": "+2",
          "scheduledDepartureTime": 1637307060000,
          "actualDepartureTime": 1637307180000,
          "showActualDepartureTime": true,
          "departureDelay": "+2"
        },
        "track": {
          "scheduled": "12",
          "actual": "12"
        },
        "info": {
          "status": 0,
          "passed": true,
          "positionStatus": "departed",
          "distance": 71274,
          "distanceFromStart": 251316
        },
        "delayReasons": null
      },
      {
        "station": {
          "evaNr": "8000036_00",
          "name": "Bielefeld Hbf",
          "code": null,
          "geocoordinates": {
            "latitude": 52.029261,
            "longitude": 8.532722
          }
        },
        "timetable": {
          "scheduledArrivalTime": 1637310060000,
          "actualArrivalTime": 1637310060000,
          "showActualArrivalTime": true,
          "arrivalDelay": "",
          "scheduledDepartureTime": 1637310180000,
          "actualDepartureTime": 1637310180000,
          "showActualDepartureTime": true,
          "departureDelay": ""
        },
        "track": {
          "scheduled": "4",
          "actual": "4"
        },
        "info": {
          "status": 0,
          "passed": false,
          "positionStatus": "future",
          "distance": 90982,
          "distanceFromStart": 342298
        },
        "delayReasons": null
      },
      {
        "station": {
          "evaNr": "8000149_00",
          "name": "Hamm (Westf) Hbf",
          "code": null,
          "geocoordinates": {
            "latitude": 51.678078,
            "longitude": 7.807821
          }
        },
        "timetable": {
          "scheduledArrivalTime": 1637311680000,
          "actualArrivalTime": 1637311800000,
          "showActualArrivalTime": true,
          "arrivalDelay": "+2",
          "scheduledDepartureTime": 1637312040000,
          "actualDepartureTime": 1637312040000,
          "showActualDepartureTime": true,
          "departureDelay": ""
        },
        "track": {
          "scheduled": "10",
          "actual": "10"
        },
        "info": {
          "status": 0,
          "passed": false,
          "positionStatus": "future",
          "distance": 63292,
          "distanceFromStart": 405590
        },
        "delayReasons": null
      },
      {
        "station": {
          "evaNr": "8000142_00",
          "name": "Hagen Hbf",
          "code": null,
          "geocoordinates": {
            "latitude": 51.362747,
            "longitude": 7.460249
          }
        },
        "timetable": {
          "scheduledArrivalTime": 1637313900000,
          "actualArrivalTime": 1637313900000,
          "showActualArrivalTime": true,
          "arrivalDelay": "",
          "scheduledDepartureTime": 1637314020000,
          "actualDepartureTime": 1637314020000,
          "showActualDepartureTime": true,
          "departureDelay": ""
        },
        "track": {
          "scheduled": "7",
          "actual": "7"
        },
        "info": {
          "status": 0,
          "passed": false,
          "positionStatus": "future",
          "distance": 42530,
          "distanceFromStart": 448120
        },
        "delayReasons": null
      },
      {
        "station": {
          "evaNr": "8000266_00",
          "name": "Wuppertal Hbf",
          "code": null,
          "geocoordinates": {
            "latitude": 51.254363,
            "longitude": 7.149543
          }
        },
        "timetable": {
          "scheduledArrivalTime": 1637314920000,
          "actualArrivalTime": 1637315040000,
          "showActualArrivalTime": true,
          "arrivalDelay": "+2",
          "scheduledDepartureTime": 1637315040000,
          "actualDepartureTime": 1637315040000,
          "showActualDepartureTime": true,
          "departureDelay": ""
        },
        "track": {
          "scheduled": "1",
          "actual": "1"
        },
        "info": {
          "status": 0,
          "passed": false,
          "positionStatus": "future",
          "distance": 24739,
          "distanceFromStart": 472859
        },
        "delayReasons": null
      },
      {
        "station": {
          "evaNr": "8000207_00",
          "name": "Köln Hbf",
          "code": null,
          "geocoordinates": {
            "latitude": 50.94303,
            "longitude": 6.958729
          }
        },
        "timetable": {
          "scheduledArrivalTime": 1637317020000,
          "actualArrivalTime": 1637317020000,
          "showActualArrivalTime": true,
          "arrivalDelay": "",
          "scheduledDepartureTime": null,
          "actualDepartureTime": null,
          "showActualDepartureTime": null,
          "departureDelay": ""
        },
        "track": {
          "scheduled": "6",
          "actual": "6"
        },
        "info": {
          "status": 0,
          "passed": false,
          "positionStatus": "future",
          "distance": 37105,
          "distanceFromStart": 509964
        },
        "delayReasons": null
      }
    ]
  },
  "connection": null,
  "selectedRoute": {
    "conflictInfo": {
      "status": "NO_CONFLICT",
      "text": null
    },
    "mobility": null
  },
  "active": null
}

````
