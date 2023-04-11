# Feature Support

:white_check_mark: Supported

:large_orange_diamond: Partially Supported

:red_circle: (Currently) Not Supported

## Query Options

### $select
:white_check_mark: Select specific properties  
:white_check_mark: Select all structural properties with the star operator  
:white_check_mark: Select properties of related entities in the Expand Options
:white_check_mark: Select navigation links  
:white_check_mark: Request all actions or functions available on every returned entity  

### $expand
:white_check_mark: Request the value of related documents to be set inline  
:white_check_mark: Request the references to the related documents to be set inline with /$ref  
:white_check_mark: Expand Options  

### $compute
:white_check_mark: Computed Properties  


### $filter
:large_orange_diamond: Filter Expressions (see Sections [Logical Operators](#logical-operators), [Arithmetic Operators](#arithmetic-operators), [Grouping](#grouping-with-parentheses) and [Functions](#functions)) for a detailed overview of supported $filter features

### $orderby
:white_check_mark: Request ascending and descending ordering
:white_check_mark: using $orderby in the Expand Options
:red_circle: Request ordering by the count of related entities or items within a collection-valued property

### $top
:white_check_mark: Request to limit the maximum number of items returned

### $skip
:white_check_mark: Request to skip the first *n* items of the query result 

### $count
:white_check_mark: Request the total count of items in a collection to be returned along with the result
:white_check_mark: Request the count of related entities within the Expand Options
### $search
:white_check_mark: Search Terms
:white_check_mark: Search Phrases
:white_check_mark: NOT-Operator
:white_check_mark: AND-Operator
:white_check_mark: OR-Operator
:large_orange_diamond: Grouping with Parentheses


## Types

:white_check_mark: Edm.Binary  
:white_check_mark:Edm.Boolean  
:red_circle: Edm.Byte  
:white_check_mark: Edm.Date  
:white_check_mark: Edm.DateTimeOffset  
:white_check_mark: Edm.Decimal  
:red_circle: Edm.Double  
:white_check_mark: Edm.Duration  
:white_check_mark: Edm.Guid  
:red_circle: Edm.Int16  
:white_check_mark: Edm.Int32  
:red_circle: Edm.Int64  
:red_circle: Edm.SByte  
:red_circle: Edm.Single  
:red_circle: Edm.Stream  
:white_check_mark: Edm.String  
:white_check_mark: Edm.TimeOfDay  
:white_check_mark: Edm.Geography  
:white_check_mark: Edm.GeographyPoint  
:white_check_mark: Edm.GeographyLineString  
:white_check_mark: Edm.GeographyPolygon  
:white_check_mark: Edm.GeographyMultiPoint  
:white_check_mark: Edm.GeographyMultiLineString  
:white_check_mark: Edm.GeographyMultiPolygon  
:white_check_mark: Edm.GeographyCollection  
:white_check_mark: Edm.Geometry  
:white_check_mark: Edm.GeometryPoint  
:white_check_mark: Edm.GeometryLineString  
:white_check_mark: Edm.GeometryPolygon  
:white_check_mark: Edm.GeometryMultiPoint  
:white_check_mark: Edm.GeometryMultiLineString  
:white_check_mark: Edm.GeometryMultiPolygon  
:white_check_mark: Edm.GeometryCollection  
## Logical Operators
### Comparison

:white_check_mark: eq (Equals)  
:white_check_mark: ne (Not Equals)  
:white_check_mark: gt (Greater Than)  
:white_check_mark: lt (Less Than)  

### Logical Expressions

:white_check_mark: and (Logical and)  
:white_check_mark: or (Logical or)  
:white_check_mark: not (Logical not)  

### Other

:white_check_mark: has (Has operator)  
:white_check_mark: in (In operator)  

## Arithmetic Operators

### Addition

:white_check_mark: add (Numeric Types)  
:large_orange_diamond: add (Date Types)  

### Subtraction

:white_check_mark: sub (Numeric Types)  
:large_orange_diamond: sub (Date Types)  

### Multiplication

:white_check_mark: mul (Numeric Types)  
:red_circle: mul (Date Types)  

### Division

:white_check_mark: div (Numeric Types)  
:red_circle: div (Date Types)  
:white_check_mark: divby (Numeric Types)  
:white_check_mark: mod (Numeric Types)  

### Negation

:white_check_mark: - (Numeric Types)  

## Grouping with parentheses

:white_check_mark: Grouping with parenthesis

## Functions
### String and Collection Functions

#### concat

:white_check_mark: concat(String, String)  
:red_circle: concat(Collection, Collection)  

#### contains

:white_check_mark: contains(String, String)  
:red_circle: contains(Collection, Collection)  

#### endswith

:white_check_mark: endswith(String, String)  
:red_circle: endswith(Collection, Collection)  

#### indexof

:white_check_mark: indexof(String, String)  
:red_circle: indexof(Collection, Collection)  

#### length

:white_check_mark: length(Edm.String)  
:red_circle: length(Collection)  

#### startswith

:white_check_mark: startswith(String, String)  
:red_circle: startswith(Collection, Collection)  

#### substring

:white_check_mark: substring(String, Number)  
:white_check_mark: substring(String, Number, Number)  
:red_circle: substring(Collection, Number)  
:red_circle: substring(Collection, Number, Number)  

### Collection Functions

:red_circle: hassubset(Collection, Collection)  
:red_circle: hassubsequence(Collection, Collection)  

### String Functions

:white_check_mark: matchesPattern(String, String)  
:white_check_mark: tolower(String)  
:white_check_mark: toupper(String)  
:white_check_mark: trim(String)  

### Date and Time Functions

:white_check_mark: date(Datetime)  
:white_check_mark: year(Date)  
:white_check_mark: year(Datetime)  
:white_check_mark: month(Date)  
:white_check_mark: month(Datetime)  
:white_check_mark: day(Date)  
:white_check_mark: day(Datetime)  
:white_check_mark: time(Date)  
:white_check_mark: time(Datetime)  
:white_check_mark: hour(Date)  
:white_check_mark: hour(Datetime)  
:white_check_mark: minute(Datetime)  
:white_check_mark: second(Datetime)  
:white_check_mark: fractionalseconds(Datetime)  
:white_check_mark: totaloffsetminutes(Datetime)  
:white_check_mark: totalseconds(Datetime)  
:white_check_mark: maxdatetime()  
:white_check_mark: now()  
:white_check_mark: mindatetime()  

### Arithmetic Functions

:white_check_mark: ceiling(Number)  
:white_check_mark: floor(Number)  
:white_check_mark: round(Number)  

### Type Functions

:white_check_mark: cast(Type)  
:white_check_mark: cast(Expression, Type)  
:white_check_mark: isof(Type)  
:white_check_mark: isof(Expression, Type)  

### Geo Functions

#### geo.distance

:white_check_mark: geo.distance(GeographyPoint, GeographyPoint)  
:white_check_mark: geo.distance(GeometryPoint, GeometryPoint)  

#### geo.intersects

:white_check_mark: geo.intersects(GeographyPoint, GeographyPolygon)  
:white_check_mark: geo.intersects(GeometryPoint, GeometryPolygon)  

#### geo.length

:white_check_mark: geo.length(GeographyLineString)  
:white_check_mark: geo.length(GeometryLineString)  

### Conditional Functions

:white_check_mark: case(Edm.Boolean:expression, ..., Edm.Boolean:expression)  

### Lambda Operators

:white_check_mark: any(Symbol:Edm.Boolean:expression)  
:white_check_mark: all(Symbol:Edm.Boolean:expression)  
