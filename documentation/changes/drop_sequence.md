---
layout: default
title: Change dropSequence
---

<!-- ====================================================== -->
<!-- GENERATED BY ChangeDocGenerator DO NOT MODIFY MANUALLY -->
<!-- ====================================================== -->

  <script>
  $(function() {
    $( "#changelog-tabs" ).tabs();
  });
</script>

# Change: 'dropSequence'

Drop an existing sequence

## Available Attributes ##

<table>
<tr><th>Name</th><th>Description</th><th>Required&nbsp;For</th><th>Supports</th><th>Since</th></tr>
<tr><td style='vertical-align: top'>catalogName</td><td style='vertical-align: top'>Name of the catalog</td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'>3.0</td></tr>
<tr><td style='vertical-align: top'>schemaName</td><td style='vertical-align: top'>Name of the schema</td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>sequenceName</td><td style='vertical-align: top'>Name of the sequence to drop</td><td style='vertical-align: top'>all</td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
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
        id="dropSequence-example"
        objectQuotingStrategy="LEGACY">
    <dropSequence catalogName="cat"
            schemaName="public"
            sequenceName="seq_id"/>
</changeSet>
{% endhighlight %}
</div>
<div id='tab-yaml'>
{% highlight yaml %}
changeSet:
  id: dropSequence-example
  author: liquibase-docs
  objectQuotingStrategy: LEGACY
  changes:
  - dropSequence:
      catalogName: cat
      schemaName: public
      sequenceName: seq_id

{% endhighlight %}
</div>
<div id='tab-json'>
{% highlight json %}
{
  "changeSet": {
    "id": "dropSequence-example",
    "author": "liquibase-docs",
    "objectQuotingStrategy": "LEGACY",
    "changes": [
      {
        "dropSequence": {
          "catalogName": "cat",
          "schemaName": "public",
          "sequenceName": "seq_id"
        }
      }]
    
  }
}

{% endhighlight %}
</div>
</div>


## SQL Generated From Above Sample (SQL Server)

{% highlight sql %}
DROP SEQUENCE [public].seq_id;


{% endhighlight %}

## Database Support

<table style='border:1;'>
<tr><th>Database</th><th>Notes</th><th>Auto Rollback</th></tr>
<tr><td>DB2</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>DB2</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Derby</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Firebird</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>H2</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>HyperSQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>INGRES</td><td>Not Supported</td><td>No</td></tr>
<tr><td>Informix</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>MariaDB</td><td>Not Supported</td><td>No</td></tr>
<tr><td>MySQL</td><td>Not Supported</td><td>No</td></tr>
<tr><td>Oracle</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>PostgreSQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>SQL Server</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>SQLite</td><td>Not Supported</td><td>No</td></tr>
<tr><td>Sybase</td><td>Not Supported</td><td>No</td></tr>
<tr><td>Sybase Anywhere</td><td><b>Supported</b></td><td>No</td></tr>
</table>
