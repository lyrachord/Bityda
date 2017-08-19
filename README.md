# Bityda
Binary Typed Data Form

# Motivation
msgpack uses self-description data form to serialize data, in which all data item is untyped.
In fact, writing data to stream, you always already know its type.
So in most cases, serializations should use strong type data form.
And because there has type tags, especially for array of item, the type overhead of data can be alleviated, as a consequence, less size to transfer, faster speed to decode
Albeit strong type used, there is still a little need to use untyped data form in some cases for convenience sake.

## Types
* there are 3 layer types 
### Strong Types
#### Type of element in an Array or Multi-Dimension Array(MDA)
  * INT1, UINT1
  * INT2, UINT2
  * INT4, UINT4, FLOAT4
  * INT8, UINT8, FLOAT8
  * INT16
  * BYTES, UTF8S
  * PAIR
  * OBJECT
#### Type of field in an Object
  * INT1, UINT1
  * INT2, UINT2
  * INT4, UINT4, FLOAT4
  * INT8, UINT8, FLOAT8
  * INT16
  * BYTES, UTF8S
  * ARRAY
  * MDA
  * UNTYPE

### Untyped
  * INT, UINT(1,2,3,4), FLOAT4
  * INT8, UINT8, FLOAT8
  * INT16
  * BYTES, UTF8S
  * ARRAY
  * MDA
  * PAIR, OBJECT
  * TRUE, FALSE
  * NIL

