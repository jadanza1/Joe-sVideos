Joe`s Videos

## Legend 

This Legend is a guide to reading and interpreting the table listings under 0NF through 3NF.

- **TableName** - Table names will be bolded and end with a colon (e.g. : `**TableName**`)

-(Column, Names) - Column names for a table will be enclosed in (rounded paranthesis).

-<b class="pk"> PrimaryKeyFields </b> - Primary key fields will be bold and insside a box.(e.g. : `<b class= "pk"> PrimaryKeyFields </b>`)

-<u class="fk"> ForeignKeyFields</u> -Foreign key fields will be a wavy underline in italic and green. (e.g.: `<u class ="fk"> ForeignKeyFields </u>`)
-<b class="rg"> {</b> Repeating Groups <b class="rg">} </b> - Groups of repeating feilds will be identified in 0NF stage, and wil lbe enclosed in ornage curly braces.(e.g.: `<b class="rg" {h </b> Repeating, Group,
 Fields <b class="rg" </b>`)


## 0NF 
**VideoRental** (<b class = "pk"> TransactionId</b>, Date, CustomerId, FirstName, LastName, Phone, StreetAddress, City, Provenice , Postalcode, <b class="rg">{ </b> VideoId, CopyNumber, Title, ReturnDate, RentalCharge, CurrentRentalCharge, <b class = "rg">}</b> Subtotal, GST, Total)

## 1NF
**VideoRental** (<b class = "pk"> TransactionId</b>, Date, CustomerIdm FirstName, LastName, Phone, StreetAddress, City, Provenice , Postalcode, Subtotal, GST, Total)
**RentalDetail**(<b class="pk"><u class="fk">TransactionId,</u> VideoId,CopyNumber </b> Title, ReturnDate, RentalChanrge, CurrentRentalCharge)

## 2NF

**RentalDetail** (<b class="pk"><u class="fk"> TransactionId</u>,<class= "pk"> VideoId, </u> CopyNumber </b>, ReturnDate, RentalCharge)

**Video**(<b class = "pk"> VideoId </b>, Title, CurrentRentalCharge)

## 3NF

**VideoRental** (<b class = "pk"> TransactionId, </b> Date, <u class = "fk" > CustomerId </u>, Subtotal, GST, Total)

**Customer** (<b class="pk"> CustomerId </b>, FirstName, LsatName, Phone, StreetAddress, City, Province , Postal Code)




----

<style =type "text/css">

.pk {
        font-weight : bold;
        display : inline-block;
        border: solid thin blue;
        padding: 0 1px;

}

.fk {
        color: green;
        font style : italic;
        text-decoration : wavy underline green;
}
.rg {
        color: darkorange;
        font-size: 1.2em;
        font weight-weight : bold;
}

