
# ChakraCore discussion 25-05-20

## 1. What is feasible before a June Release

See previous plan: https://github.com/chakra-core/org/blob/master/Release%201.12%20plan.md

- Feature work
- Testing
- Release channel

## 2. API shape considerations

- What should we aim at with APIs - a large number of granular/narrow methods OR a smaller number of multi-purpose methods?
- What should we do with undocumented APIs - see list below.
- SHould we re-work the module API?
- Any other specific considerations?

## 3. Availability and plans

- How much time do team members have to contribute in the next month?
- What specific pieces of work do team members wish do contribute to?

## List of undocumented APIs

- JsCloneObject
- JsCreateCustomExternalObject
- JsCreatePropertyString
- JsCreateTracedExternalObject
- JsDeserializeParserState
- JsDetachArrayBuffer
- JsDiscardBackgroundParse_Experimental
- JsExecuteBackgroundParse_Experimental
- JsExperimentalApiRunModule
- JsExternalizeArrayBuffer
- JsGetArrayBufferExtraInfo
- JsGetArrayBufferFreeFunction
- JsGetArrayEntriesFunction
- JsGetArrayForEachFunction
- JsGetArrayKeysFunction
- JsGetArrayValuesFunction
- JsGetEmbedderData
- JsGetErrorPrototype
- JsGetIteratorPrototype
- JsGetPropertyIdSymbolIterator
- JsHasOwnItem
- JsIsCallable
- JsIsConstructor
- JsObjectDefinePropertyFull
- JsPrivateDeleteProperty
- JsPrivateGetProperty
- JsPrivateHasProperty
- JsPrivateSetProperty
- JsQueueBackgroundParse_Experimental
- JsSetArrayBufferExtraInfo
- JsSetEmbedderData
- JsVarDeserializerFree
- JsVarDeserializerReadBytes
- JsVarDeserializerReadRawBytes
- JsVarDeserializerReadValue
- JsVarDeserializerSetTransferableVars
- JsVarDeserializer
- JsVarSerializerDetachArrayBuffer
- JsVarSerializerFree
- JsVarSerializerReleaseData
- JsVarSerializerSetTransferableVars
- JsVarSerializerWriteRawBytes
- JsVarSerializerWriteValue
- JsVarSerializer
