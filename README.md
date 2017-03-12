# Command line <A HREF="https://en.wikipedia.org/wiki/Rail_Baron">Rail Baron</A> utilities

## roll and payout

These are simple command line utilities written in perl to do payout
lookups and roll destinations in a game of <A
HREF="https://en.wikipedia.org/wiki/Rail_Baron">Rail Baron</A>.

They are nice to play the game without using the awkward paper lookup tables.

payout needs the "Payout.csv" file that is here, as well as the Text::CSV
perl module that if you don't have it you can install from CPAN.

## Example

Alice is playing and arrives in Tucumcari, having started in New York, and
needs to get paid, so she runs "payout"

```
$ ./payout "New York" "Tucumcari"
Payout for New York to Tucumcari is 20.0
```
And Alice receives $20,000 for her trip.

Later needing to go to a new destination she runs "roll":

```
$ ./roll
Region: SouthWest City: Las Vegas
```

Since Alice is in the SouthWest region (In Tucumcari), she is now permitted to
choose the region in which her destinaiton will be. Since her evil opponent Bob
has bought up the NorthEast railroads, she chooses SouthEast:

```
$ ./roll SouthEast
Region: SouthEast City: Miami
```

Now Alice is going to Miami.
