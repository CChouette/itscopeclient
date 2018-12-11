# ProductType

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Eindeutiger Key | 
**product_type_group** | [**\Swagger\Client\Model\ProductTypeGroup**](ProductTypeGroup.md) | Referenz auf Produkttyp-Gruppe (ProductTypeGroup.id, n:1) | 
**name** | **string** | Bezeichner des Produkttyps. Kann als 2. &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/207249385\&quot;&gt;Kategorieebene&lt;/a&gt; verwendet werden. | 
**attribute_type_id1** | **int** | Eindeutiger Attribut Key, um eine mögliche Unterkategorie aufzubauen, verweist 1:n auf AttributeCluster.attributeTypeId | [optional] 
**attribute_type_name1** | **string** | Bezeichner des Attributes, um eine mögliche Unterkategorie aufzubauen | [optional] 
**attribute_type_id2** | **int** | Eindeutiger Attribut Key, um eine mögliche Unterkategorie aufzubauen, verweist 1:n auf AttributeCluster.attributeTypeId | [optional] 
**attribute_type_name2** | **string** | Bezeichner des Attributes, um eine mögliche Unterkategorie aufzubauen | [optional] 
**attribute_type_id3** | **int** | Eindeutiger Attribut Key, um eine mögliche Unterkategorie aufzubauen, verweist 1:n auf AttributeCluster.attributeTypeId | [optional] 
**attribute_type_name3** | **string** | Bezeichner des Attributes, um eine mögliche Unterkategorie aufzubauen | [optional] 
**attribute_type_id4** | **int** | Eindeutiger Attribut Key, um eine mögliche Unterkategorie aufzubauen, verweist 1:n auf AttributeCluster.attributeTypeId | [optional] 
**attribute_type_name4** | **string** | Bezeichner des Attributes, um eine mögliche Unterkategorie aufzubauen | [optional] 
**attribute_type_id5** | **int** | Eindeutiger Attribut Key, um eine mögliche Unterkategorie aufzubauen, verweist 1:n auf AttributeCluster.attributeTypeId | [optional] 
**attribute_type_name5** | **string** | Bezeichner des Attributes, um eine mögliche Unterkategorie aufzubauen | [optional] 
**attribute_type** | [**\Swagger\Client\Model\AttributeType[]**](AttributeType.md) | Konkrete Eigenschaftstypen von Produkteigenschaften. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


