---
layout: default
title: Change modifyDataType
---

<!-- ====================================================== -->
<!-- GENERATED BY ChangeDocGenerator DO NOT MODIFY MANUALLY -->
<!-- ====================================================== -->

  <script>
  $(function() {
    $( "#changelog-tabs" ).tabs();
  });
</script>

# Change: 'modifyDataType'

Modify data type

## Available Attributes ##

<table>
<tr><th>Name</th><th>Description</th><th>Required&nbsp;For</th><th>Supports</th><th>Since</th></tr>
<tr><td style='vertical-align: top'>catalogName</td><td style='vertical-align: top'>Name of the catalog</td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'>3.0</td></tr>
<tr><td style='vertical-align: top'>columnName</td><td style='vertical-align: top'>Name of the column</td><td style='vertical-align: top'>all</td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>newDataType</td><td style='vertical-align: top'></td><td style='vertical-align: top'>all</td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>schemaName</td><td style='vertical-align: top'>Name of the schema</td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>tableName</td><td style='vertical-align: top'>Name of the table</td><td style='vertical-align: top'>all</td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
</table>

<div id='changelog-tabs'>
<ul>
    <li><a href="#tab-xml">XML Sample</a></li>
    <li><a href="#tab-yaml">YAML Sample</a></li>
    <li><a href="#tab-json">JSON Sample</a></li>
  </ul>
<div id='tab-xml'>
{% highlight xml %}
<changeSet author="liquibase-docs"
        id="modifyDataType-example"
        objectQuotingStrategy="LEGACY">
    <modifyDataType catalogName="cat"
            columnName="id"
            newDataType="int"
            schemaName="public"
            tableName="person"/>
</changeSet>
{% endhighlight %}
</div>
<div id='tab-yaml'>
{% highlight yaml %}
changeSet:
  id: modifyDataType-example
  author: liquibase-docs
  objectQuotingStrategy: LEGACY
  changes:
  - modifyDataType:
      catalogName: cat
      columnName: id
      newDataType: int
      schemaName: public
      tableName: person

{% endhighlight %}
</div>
<div id='tab-json'>
{% highlight json %}
{
  "changeSet": {
    "id": "modifyDataType-example",
    "author": "liquibase-docs",
    "objectQuotingStrategy": "LEGACY",
    "changes": [
      {
        "modifyDataType": {
          "catalogName": "cat",
          "columnName": "id",
          "newDataType": "int",
          "schemaName": "public",
          "tableName": "person"
        }
      }]
    
  }
}

{% endhighlight %}
</div>
</div>


## SQL Generated From Above Sample (MySQL)

{% highlight sql %}
ALTER TABLE cat.person MODIFY id INT;


{% endhighlight %}

## Database Support

<table style='border:1;'>
<tr><th>Database</th><th>Notes</th><th>Auto Rollback</th></tr>
<tr><td>DB2</td><td>Not Supported</td><td>No</td></tr>
<tr><td>DB2</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Derby</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Firebird</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>H2</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>HyperSQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>INGRES</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Informix</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>MariaDB</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>MySQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Oracle</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>PostgreSQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>SQL Server</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>SQLite</td><td>Not Supported</td><td>No</td></tr>
<tr><td>Sybase</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Sybase Anywhere</td><td><b>Supported</b></td><td>No</td></tr>
</table>
