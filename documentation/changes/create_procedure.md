---
layout: default
title: Change createProcedure
---

<!-- ====================================================== -->
<!-- GENERATED BY ChangeDocGenerator DO NOT MODIFY MANUALLY -->
<!-- ====================================================== -->

  <script>
  $(function() {
    $( "#changelog-tabs" ).tabs();
  });
</script>

# Change: 'createProcedure'

Defines the definition for a stored procedure. This command is better to use for creating procedures than the raw sql command because it will not attempt to strip comments or break up lines.

Often times it is best to use the CREATE OR REPLACE syntax along with setting runOnChange='true' on the enclosing changeSet tag. That way if you need to make a change to your procedure you can simply change your existing code rather than creating a new REPLACE PROCEDURE call. The advantage to this approach is that it keeps your change log smaller and allows you to more easily see what has changed in your procedure code through your source control system's diff command.

## Available Attributes ##

<table>
<tr><th>Name</th><th>Description</th><th>Required&nbsp;For</th><th>Supports</th><th>Since</th></tr>
<tr><td style='vertical-align: top'>catalogName</td><td style='vertical-align: top'>Name of the catalog</td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>comments</td><td style='vertical-align: top'></td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>dbms</td><td style='vertical-align: top'></td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'>3.1</td></tr>
<tr><td style='vertical-align: top'>encoding</td><td style='vertical-align: top'></td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>path</td><td style='vertical-align: top'>File containing the procedure text. Either this attribute or a nested procedure text is required.</td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>procedureText</td><td style='vertical-align: top'></td><td style='vertical-align: top'>all</td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>procedureName</td><td style='vertical-align: top'></td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>relativeToChangelogFile</td><td style='vertical-align: top'></td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>replaceIfExists</td><td style='vertical-align: top'></td><td style='vertical-align: top'></td><td style='vertical-align:top'>mssql</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>schemaName</td><td style='vertical-align: top'>Name of the schema</td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
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
        id="createProcedure-example"
        objectQuotingStrategy="LEGACY">
    <createProcedure catalogName="cat"
            comments="A String"
            dbms="h2, oracle"
            encoding="UTF-8"
            path="com/example/my-logic.sql"
            procedureName="new_customer"
            relativeToChangelogFile="true"
            replaceIfExists="false"
            schemaName="public">CREATE OR REPLACE PROCEDURE testHello
    IS
    BEGIN
      DBMS_OUTPUT.PUT_LINE('Hello From The Database!');
    END;</createProcedure>
</changeSet>
{% endhighlight %}
</div>
<div id='tab-yaml'>
{% highlight yaml %}
changeSet:
  id: createProcedure-example
  author: liquibase-docs
  objectQuotingStrategy: LEGACY
  changes:
  - createProcedure:
      catalogName: cat
      comments: A String
      dbms: h2, oracle
      encoding: UTF-8
      path: com/example/my-logic.sql
      procedureText: |-
        CREATE OR REPLACE PROCEDURE testHello
            IS
            BEGIN
              DBMS_OUTPUT.PUT_LINE('Hello From The Database!');
            END;
      procedureName: new_customer
      relativeToChangelogFile: true
      replaceIfExists: false
      schemaName: public

{% endhighlight %}
</div>
<div id='tab-json'>
{% highlight json %}
{
  "changeSet": {
    "id": "createProcedure-example",
    "author": "liquibase-docs",
    "objectQuotingStrategy": "LEGACY",
    "changes": [
      {
        "createProcedure": {
          "catalogName": "cat",
          "comments": "A String",
          "dbms": "h2, oracle",
          "encoding": "UTF-8",
          "path": "com/example/my-logic.sql",
          "procedureText": "CREATE OR REPLACE PROCEDURE testHello\n    IS\n    BEGIN\n      DBMS_OUTPUT.PUT_LINE('Hello From The Database!');\n    END;",
          "procedureName": "new_customer",
          "relativeToChangelogFile": true,
          "replaceIfExists": false,
          "schemaName": "public"
        }
      }]
    
  }
}

{% endhighlight %}
</div>
</div>


## Database Support

<table style='border:1;'>
<tr><th>Database</th><th>Notes</th><th>Auto Rollback</th></tr>
<tr><td>DB2</td><td><b>Supported</b></td><td>No</td></tr>
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
<tr><td>SQLite</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Sybase</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Sybase Anywhere</td><td><b>Supported</b></td><td>No</td></tr>
</table>
