<h1>SPC Chart</h1>

<p>
  <small>Developed by University Hospitals Group Liverpool</small>
</p>

<h3>
  A Power BI custom visual for Statistical Process Control,
  designed to support NHS Making Data Count principles.
</h3>

<p>
  The SPC Chart helps users understand variation and performance
  over time through dynamically calculated Statistical Process
  Control charts. It can be used with simple datasets or extended
  with targets, step changes and supplied control limits.
</p>

<h2>Features</h2>

<ul>
  <li>Dynamic SPC control limits and centre line</li>
  <li>Optional supplied Upper and Lower Control Limits (UCL/LCL)</li>
  <li>Optional targets and target direction</li>
  <li>Automatic step-change calculation</li>
  <li>SPC special-cause rules</li>
  <li>Variation and assurance indicators</li>
  <li>Interactive <strong>What-if analysis</strong></li>
  <li>Drag control limits to explore alternative scenarios</li>
  <li>Ghost individual observations from exploratory calculations</li>
  <li>Add or move an exploratory step change</li>
  <li>Dynamically recalculate SPC following exploratory changes</li>
  <li>Reset exploratory analysis to the original configuration</li>
</ul>

<hr>

<h2>Getting Started</h2>

<p>
  The SPC Chart requires a minimum of two data fields:
  <strong>Date</strong> and <strong>Value</strong>.
  All other fields are optional.
</p>

<p>
  When control limits and a centre line are not supplied, the visual
  calculates the SPC analysis dynamically from the data. This allows
  the chart to respond to Power BI filters and selections.
</p>

<h3>Minimum Data</h3>

<table>
  <thead>
    <tr>
      <th>Field</th>
      <th>Required</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Date</strong></td>
      <td>Yes</td>
      <td>
        A valid date field used to display observations in chronological order.
      </td>
    </tr>
    <tr>
      <td><strong>Value</strong></td>
      <td>Yes</td>
      <td>
        A numeric measure or percentage representing the process being monitored.
      </td>
    </tr>
  </tbody>
</table>

<h3>Optional Data Fields</h3>

<table>
  <thead>
    <tr>
      <th>Field</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Target</strong></td>
      <td>
        An optional target value used for the target line and assurance indicator.
      </td>
    </tr>
    <tr>
      <td><strong>Target Direction</strong></td>
      <td>
        Defines whether higher or lower values represent better performance.
        <strong>U</strong> = higher is good,
        <strong>D</strong> = lower is good and
        <strong>N</strong> = no target set.
      </td>
    </tr>
    <tr>
      <td><strong>Step Change</strong></td>
      <td>
        Use <strong>0</strong> for normal observations and
        <strong>1</strong> where a new process segment should begin.
        The visual recalculates the centre line and control limits for
        the new segment.
      </td>
    </tr>
    <tr>
      <td><strong>Upper Control Limit</strong></td>
      <td>
        An optional supplied Upper Control Limit. When supplied, it is
        used instead of the automatically calculated UCL for the
        standard chart.
      </td>
    </tr>
    <tr>
      <td><strong>Lower Control Limit</strong></td>
      <td>
        An optional supplied Lower Control Limit. When supplied, it is
        used instead of the automatically calculated LCL for the
        standard chart.
      </td>
    </tr>
    <tr>
      <td><strong>Number Format</strong></td>
      <td>
        Optional formatting override. Use N0, N1 or N2 for numbers,
        or P0, P1 or P2 for percentages.
      </td>
    </tr>
  </tbody>
</table>

<h3>Number Formats</h3>

<table>
  <thead>
    <tr>
      <th>Format</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>N0</strong></td>
      <td>Number with 0 decimal places</td>
    </tr>
    <tr>
      <td><strong>N1</strong></td>
      <td>Number with 1 decimal place</td>
    </tr>
    <tr>
      <td><strong>N2</strong></td>
      <td>Number with 2 decimal places</td>
    </tr>
    <tr>
      <td><strong>P0</strong></td>
      <td>Percentage with 0 decimal places</td>
    </tr>
    <tr>
      <td><strong>P1</strong></td>
      <td>Percentage with 1 decimal place</td>
    </tr>
    <tr>
      <td><strong>P2</strong></td>
      <td>Percentage with 2 decimal places</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>Format Options</h2>

<p>
  The Format pane provides options for controlling the appearance and
  behaviour of the SPC Chart. These settings allow the visual to be
  adapted to different reporting requirements without changing the
  underlying Power BI data.
</p>

<h3>Icon Options</h3>

<p>
  Icon Options control the variation and assurance indicators displayed
  alongside the chart.
</p>

<table>
  <thead>
    <tr>
      <th>Option</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Show Icons</strong></td>
      <td>
        Shows or hides the variation and assurance indicators displayed
        alongside the chart.
      </td>
    </tr>
    <tr>
      <td><strong>Icon Size</strong></td>
      <td>
        Controls the size of the icons. Available options are
        <strong>Small</strong>, <strong>Medium</strong> and
        <strong>Large</strong>.
      </td>
    </tr>
    <tr>
      <td><strong>Pane Style</strong></td>
      <td>
        Controls how much information is displayed alongside the icons.
        <strong>Minimal</strong> displays the icons only,
        <strong>Standard</strong> displays the icons and values, and
        <strong>Detailed</strong> displays the icons, values and
        descriptive information.
      </td>
    </tr>
    <tr>
      <td><strong>Hide Assurance Icon if No Target</strong></td>
      <td>
        Hides the assurance icon when no target is available.
        This is useful where the chart is being used to assess
        variation without a performance target.
      </td>
    </tr>
  </tbody>
</table>

<h3>Target Options</h3>

<table>
  <thead>
    <tr>
      <th>Option</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Show Target Line</strong></td>
      <td>
        Shows or hides the target line on the chart.
        Hiding the target line does not prevent the target from
        being used for assurance calculations.
      </td>
    </tr>
    <tr>
      <td><strong>Target Direction</strong></td>
      <td>
        Defines which direction represents better performance.
        <strong>High is good</strong> means higher values are desirable.
        <strong>Low is good</strong> means lower values are desirable.
        <strong>No target set</strong> disables target-based assurance.
      </td>
    </tr>
  </tbody>
</table>

<h3>Data Options</h3>

<table>
  <thead>
    <tr>
      <th>Option</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Point Size</strong></td>
      <td>
        Controls the size of the observations displayed on the chart.
        Available options are <strong>Small</strong>,
        <strong>Medium</strong> and <strong>Large</strong>.
      </td>
    </tr>
  </tbody>
</table>

<h3>SPC Rules</h3>

<p>
  The SPC Chart identifies special-cause variation using four
  configurable SPC rules. Each rule can be independently enabled
  or disabled.
</p>

<table>
  <thead>
    <tr>
      <th>Rule</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <strong>Rule 1: Point beyond control limits</strong>
      </td>
      <td>
        Identifies an individual observation above the Upper Control
        Limit or below the Lower Control Limit.
      </td>
    </tr>
    <tr>
      <td>
        <strong>Rule 2: 2 of 3 near control limits</strong>
      </td>
      <td>
        Identifies two or more of three consecutive observations
        beyond the two-sigma zone on the same side of the centre line,
        while remaining within the corresponding control limit.
      </td>
    </tr>
    <tr>
      <td>
        <strong>Rule 3: 7-point trend</strong>
      </td>
      <td>
        Identifies a run of seven or more consecutive observations
        continuously increasing or continuously decreasing.
      </td>
    </tr>
    <tr>
      <td>
        <strong>Rule 4: 7 on same side of mean</strong>
      </td>
      <td>
        Identifies seven or more consecutive observations above or
        below the process mean. Observations equal to the mean do not
        contribute to the run.
      </td>
    </tr>
  </tbody>
</table>

<p>
  Configured step changes reset the appropriate rule sequences so that
  observations from different process segments are not incorrectly
  assessed as a continuous run.
</p>

<p>
  Disabling a rule prevents that rule from contributing to the
  variation classification.
</p>

<h3>X-Axis Options</h3>

<table>
  <thead>
    <tr>
      <th>Option</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Date Format</strong></td>
      <td>
        Controls how dates are displayed on the X axis.
        Available formats are <strong>DD/MM/YYYY</strong>,
        <strong>MMM YYYY</strong>, <strong>DD MMM</strong>
        and <strong>DD MMM YY</strong>.
      </td>
    </tr>
    <tr>
      <td><strong>Hide Title</strong></td>
      <td>
        Hides the <strong>Date</strong> title displayed beneath
        the X axis.
      </td>
    </tr>
  </tbody>
</table>

<h3>Y-Axis Options</h3>

<table>
  <thead>
    <tr>
      <th>Option</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Ignore Below 0</strong></td>
      <td>
        Sets the minimum value of the Y axis to zero.
        This is useful where negative values are not meaningful,
        particularly where a statistically calculated Lower Control
        Limit would otherwise fall below zero.
      </td>
    </tr>
  </tbody>
</table>

<hr>

<h2>Using Explore</h2>

<p>
  The <strong>Explore</strong> function provides an interactive way to
  investigate how changes to observations, process segmentation or
  control limits could affect the SPC analysis.
</p>

<p>
  Explore is designed for <strong>what-if analysis</strong>.
  It does not change the underlying Power BI data or the configured
  SPC analysis. Changes made while exploring are temporary and can
  be removed using <strong>Reset</strong>.
</p>

<h3>Starting Explore</h3>

<p>
  Select <strong>Explore limits</strong> to enter exploratory mode.
</p>

<p>
  When Explore is first opened, the chart retains the control limits
  currently being displayed. This includes supplied UCL and LCL values
  where these have been provided.
</p>

<p>
  Once an observation is ghosted or an exploratory step change is
  introduced, the visual recalculates the SPC limits from the
  underlying observations using the exploratory configuration.
</p>

<h3>Moving the Control Limits</h3>

<p>
  When Explore is active, handles are provided for the
  <strong>Upper Control Limit (UCL)</strong> and
  <strong>Lower Control Limit (LCL)</strong>.
</p>

<ul>
  <li>Drag the UCL handle up or down to explore an alternative upper limit.</li>
  <li>Drag the LCL handle up or down to explore an alternative lower limit.</li>
  <li>The control limits cannot be moved through the process mean.</li>
</ul>

<p>
  As the limits are moved, the SPC rules and variation assessment are
  recalculated automatically.
</p>

<h3>Ghosting an Observation</h3>

<p>
  Individual observations can be temporarily excluded from the
  exploratory calculation without removing them from the chart.
</p>

<ol>
  <li>Right-click the observation you want to investigate.</li>
  <li>Select <strong>Ghost point</strong>.</li>
  <li>
    The observation remains visible but is excluded from the
    exploratory SPC calculation.
  </li>
</ol>

<p>
  Ghosted observations are also excluded from the exploratory SPC
  rule assessment. The control limits are recalculated using the
  remaining observations.
</p>

<p>
  This allows users to investigate questions such as whether an
  unusual observation is having a significant effect on the process
  limits.
</p>

<p>
  To include the observation again, right-click the ghosted point and
  select <strong>Restore point</strong>.
</p>

<h3>Adding an Exploratory Step Change</h3>

<p>
  Explore can also be used to investigate the effect of a potential
  process change.
</p>

<ol>
  <li>
    Right-click the observation where you want the potential new
    process segment to begin.
  </li>
  <li>Select <strong>Add step change</strong>.</li>
  <li>
    The visual recalculates the SPC analysis using the new exploratory
    process segment.
  </li>
</ol>

<p>
  The exploratory step change does not modify step changes supplied
  through the underlying data.
</p>

<p>
  Only one exploratory step change can be added at a time.
  If one already exists, right-click another observation and select
  <strong>Move step change here</strong> to investigate a different
  location.
</p>

<h3>Existing Step Changes</h3>

<p>
  Step changes already configured through the data are retained while
  using Explore.
</p>

<p>
  An exploratory step change is added to the existing process structure
  rather than replacing configured step changes. This allows an
  additional potential process change to be investigated while
  preserving the original analysis.
</p>

<h3>Combining Explore Functions</h3>

<p>
  Explore functions can be used together.
</p>

<p>
  For example, an unusual observation can first be ghosted and the
  resulting control limits examined. An exploratory step change can
  then be introduced to investigate whether the subsequent observations
  represent a different process.
</p>

<p>
  The control limits and SPC assessment are dynamically recalculated
  as the exploratory analysis changes.
</p>

<h3>Exploratory Status</h3>

<p>
  While Explore is active, the visual displays an exploratory status
  indicator to help distinguish the exploratory analysis from the
  original configured SPC analysis.
</p>

<p>
  The status can also indicate when observations have been excluded
  or the control limits have been adjusted.
</p>

<h3>Resetting the Analysis</h3>

<p>
  Select <strong>Reset</strong> to remove the exploratory changes.
</p>

<p>Reset removes:</p>

<ul>
  <li>Adjusted UCL and LCL positions</li>
  <li>Ghosted observations</li>
  <li>The exploratory step change</li>
</ul>

<p>
  The chart then returns to its original configured analysis,
  including supplied control limits and configured step changes.
</p>

<p>
  Explore is intended as an investigative tool. It does not
  retrospectively modify the underlying observations or configured
  SPC analysis.
</p>

<hr>

<h2>What is an SPC Chart?</h2>

<p>
  Statistical Process Control (SPC) is a method of understanding how
  a process behaves over time. Data is plotted in time order alongside
  statistically derived control limits, allowing normal process
  variation to be distinguished from signals that may indicate a
  meaningful change.
</p>

<h3>What You Will See</h3>

<ol>
  <li>
    <strong>Data Points</strong> – individual measurements or results
    from the process being monitored.
  </li>

  <li>
    <strong>Control Limits</strong> – the Upper Control Limit (UCL)
    and Lower Control Limit (LCL) describe the expected range of
    variation in the process.
  </li>

  <li>
    <strong>Centre Line</strong> – represents the process mean for
    the relevant process segment.
  </li>

  <li>
    <strong>Target Line</strong> – an optional performance target
    against which assurance can be assessed.
  </li>

  <li>
    <strong>Variation and Assurance Indicators</strong> – provide
    a summary of how the process is behaving and, where a target is
    available, its ability to consistently achieve that target.
  </li>
</ol>

<h2>Variation</h2>

<p>
  Variation describes whether the process appears to be behaving
  normally or whether there is evidence of special-cause variation.
</p>

<table>
  <thead>
    <tr>
      <th>Classification</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Common Cause</strong></td>
      <td>
        The process is displaying its expected level of variation with
        no significant special-cause signal identified.
      </td>
    </tr>
    <tr>
      <td><strong>Improvement</strong></td>
      <td>
        Special-cause variation has been identified in a direction
        associated with improved performance.
      </td>
    </tr>
    <tr>
      <td><strong>Concern</strong></td>
      <td>
        Special-cause variation has been identified in a direction
        associated with poorer performance or increased pressure.
      </td>
    </tr>
  </tbody>
</table>

<h2>Assurance</h2>

<p>
  Assurance considers the relationship between the process control
  limits and the target. It provides an indication of whether the
  process is capable of consistently achieving the target.
</p>

<table>
  <thead>
    <tr>
      <th>Classification</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Passing</strong></td>
      <td>
        The process is consistently capable of meeting the target.
      </td>
    </tr>
    <tr>
      <td><strong>Inconsistent</strong></td>
      <td>
        The process may meet or miss the target and cannot be expected
        to do so consistently.
      </td>
    </tr>
    <tr>
      <td><strong>Failing</strong></td>
      <td>
        The process is consistently unlikely to achieve the target.
      </td>
    </tr>
  </tbody>
</table>

<hr>

<h2>Why Use an SPC Chart?</h2>

<p>
  SPC charts help users understand the story behind performance data
  rather than reacting to individual values in isolation.
</p>

<ul>
  <li>
    <strong>Identify meaningful change</strong> – recognise signals
    that may indicate something different is happening in the process.
  </li>

  <li>
    <strong>Understand variation</strong> – distinguish expected
    process fluctuation from special-cause variation.
  </li>

  <li>
    <strong>Track performance over time</strong> – understand whether
    a process is stable, improving or deteriorating.
  </li>

  <li>
    <strong>Avoid overreaction</strong> – reduce unnecessary responses
    to normal random variation.
  </li>

  <li>
    <strong>Support improvement</strong> – use evidence of process
    change to support investigation and decision-making.
  </li>
</ul>

<hr>

<h2>Making Data Count</h2>

<p>
  Making Data Count encourages NHS organisations to use data in a way
  that better supports understanding, decision-making and improvement.
  Statistical Process Control is a key part of this approach.
</p>

<h3>Understanding Variation</h3>

<p>
  SPC helps distinguish between <strong>common-cause variation</strong>,
  which represents the normal variation inherent in a process, and
  <strong>special-cause variation</strong>, which may indicate that
  something different has happened.
</p>

<p>
  Understanding this distinction can help teams avoid reacting to every
  change in a measure and instead focus attention where the data provides
  evidence of a meaningful change.
</p>

<h3>Moving Beyond RAG</h3>

<p>
  Traditional Red, Amber and Green reporting can focus attention on
  whether an individual value has crossed a threshold without showing
  how the process has behaved over time.
</p>

<p>
  SPC adds this context by displaying the process history, expected
  variation and signals of change.
</p>

<h3>Supporting Decision-Making</h3>

<p>
  By distinguishing expected variation from significant change, SPC can
  help teams decide when investigation or action may be appropriate and
  when a change is more likely to represent normal process variation.
</p>

<h3>Building a Culture of Improvement</h3>

<p>
  Making Data Count encourages teams to be curious about their data and
  ask questions such as:
</p>

<ul>
  <li>What is the data telling us?</li>
  <li>Is the process behaving differently?</li>
  <li>What may be driving the change?</li>
  <li>Is an intervention having the intended effect?</li>
  <li>What can we do to improve the process?</li>
</ul>

<h3>Example NHS Applications</h3>

<ul>
  <li>
    <strong>Waiting Times</strong> – monitor waiting times and identify
    sustained changes following improvement interventions.
  </li>

  <li>
    <strong>Patient Safety</strong> – monitor measures such as incidents
    or infection rates and identify unusual process behaviour.
  </li>

  <li>
    <strong>Operational Performance</strong> – understand changes in
    demand, flow and service performance.
  </li>

  <li>
    <strong>Resource Planning</strong> – monitor measures such as bed
    availability, activity or staffing over time.
  </li>
</ul>

<hr>

<h2>Important Note</h2>

<p>
  SPC signals should be interpreted alongside appropriate operational,
  clinical and organisational context. The visual supports analysis and
  investigation but does not determine the cause of a change or replace
  professional judgement.
</p>

<hr>

<p>
  <small>
    SPC Chart – Developed by University Hospitals Group Liverpool
  </small>
</p>
