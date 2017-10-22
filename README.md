# TypeScript library for OpenCPU
Forked from https://github.com/NextCenturyCorporation/opencpu.js
to make use of ES6 and TypeScript.

## Installation
`npm install --save y0hy0h/opencpu-ts`

## Usage
<table>
    <tr>
        <td><code>import { OpenCPU } from 'opencpu-ts'</code></td>
        <td>Import the library</td>
    </tr>
    <tr>
        <td><code>const opencpu = new OpenCPU()</code></td>
        <td>Instantiate a new object</td>
    </tr>
    <tr>
        <td><code>await opencpu.setUrl('https://cloud.opencpu.org/ocpu/library/MASS/')</code></td>
        <td>Set the URL to the <code>base</code> package on the public server</td>
   </tr>
   <tr>
        <td><code>const session = await opencpu.call('print', {x: [1,2,3]})</code></td>
        <td>Call <code>print(x=list(1,2,3))</code></td>
   </tr>
   <tr>
        <td><code>const returnValue = await session.getObject()</code></td>
        <td>Get the return value (note that <code>print</code> also returns the value)</td>
   </tr>
   <tr>
        <td><code>const consoleOutput = await session.get('stdout').then(response => response.text())</code></td>
        <td>Read the console output</td>
   </tr>
</table>

