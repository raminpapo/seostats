# PHP Class SEOstats #


---

## Important Update ##

The project page moved to GitHub! To download the latest version, please visit https://github.com/eyecatchup/SEOstats

The documentation will stay for whatever reason, but no longer be updated.<br>Issue must be reported to GitHub, too.<br>
<br>
Best regards,<br>
Stephan.<br>
<hr />
<h2>Project Description</h2>

SEOstats is a powerful open source PHP class to get a lot of SEO relevant data such as detailed backlink analyses,<br>keyword and traffic statistics, website trends, page authority, the Google Pagerank, the Alexa Trafficrank and much more.<br><br>Therefore SEOstats gathers data from Google, Yahoo, Bing, Majesticseo, SEOmoz, Alexa, Facebook and Twitter. SEOstats offers over 50 different methods to request SEO relevant data for websites.<br>
<hr />
<h2>Table of Contents</h2>
<br>
<hr />
<h2>Demo</h2>
Two live demos are available at:<br>
<ul><li><a href='http://demos.bexton.net/seostats/index.php'>http://demos.bexton.net/seostats/index.php</a>
</li><li><a href='http://demos.bexton.net/seostats/demo.html'>http://demos.bexton.net/seostats/demo.html</a></li></ul>

There is also an iframe based Facebook App Version of the demo, that can be used as a custom tab to your Facebook profile page.<br>Therefore use the "Add to my page" link on the apps' profile page (2nd link).<br>
<ul><li><a href='http://apps.facebook.com/seo-check/'>http://apps.facebook.com/seo-check/</a>
</li><li><a href='http://www.facebook.com/apps/application.php?id=181872768521082&sk=app_181872768521082'>http://www.facebook.com/apps/application.php?id=181872768521082&amp;sk=app_181872768521082</a>
<hr />
<h2>Feature Requests</h2>
New feature requests can be placed at: <a href='http://bexton.net/php-class-seostats/'>http://bexton.net/php-class-seostats/</a>
<hr />
<h2>Back-to-Back Credit</h2>
The usage of SEOstats is completely free.</li></ul>

But as a little back-to-back credit, i appreciate when you give me a backlink to my business site from any of your projects.<br>
You will find pre-formed backlinks at <a href='http://www.nahklick.de/backlinks/'>http://www.nahklick.de/backlinks/</a>

Thank you!<br>
<hr />
<h2>Download</h2>
Direct link to the latest version: <a href='https://github.com/eyecatchup/SEOstats/zipball/master'>https://github.com/eyecatchup/SEOstats/zipball/master</a>

<hr />

<h1>How To Use</h1>

<h2>Example Code</h2>
<pre><code>&lt;?php include '../src/class.seostats.php';<br>
<br>
try <br>
{<br>
	$url = new SEOstats($_GET['url']);<br>
	$url-&gt;print_array('Google','json');<br>
<br>
} <br>
catch (SEOstatsException $e) <br>
{<br>
	die($e-&gt;getMessage());<br>
}<br>
?&gt;<br>
</code></pre>
More example files are included within the download archive!<br>
<br>
<b>NOTE:</b> The Pagerank Checksum API URL was going to be changed anyway with the next release. As the old URL stopped working (for any reason i don't have the time to determine now), you can use the new URL, that will be implemented with the next version's release as standard anyway. Therefore you have to change the line:<br>
<blockquote><code>const PAGERANK_CHECKSUM_API_URI = 'http://217.150.244.124/prch/?url=';</code>
to<br>
<code>const PAGERANK_CHECKSUM_API_URI = 'http://pagerank.bexton.net/?url=';</code>
in the second line of the <a href='http://code.google.com/p/seostats/#class.seostats.php'>main class (file: <code>class.seostats.php</code>)</a>
<hr />
<h2>Public Methods (Feature List)</h2></blockquote>

<h3>Google Methods</h3>

<table><thead><th> <b>Method</b> </th><th> <b>@return</b> </th></thead><tbody>
<tr><td> <code>Google()</code> </td><td> Returns an array, containing all results of all Google methods. </td></tr>
<tr><td> <code>Google_Page_Rank()</code> </td><td> Returns the Google PageRank. </td></tr>
<tr><td> <code>Google_Siteindex_Total()</code> </td><td> Returns the total amount of results for a Google 'site:'-search on the object URL. </td></tr>
<tr><td> <code>Google_Siteindex_Total_API()</code> <b>new</b> </td><td> Same like Google_Siteindex_Total, but requesting data from the Websearch API. </td></tr>
<tr><td> <code>Google_Siteindex_Array()</code> </td><td> Returns an array, containing the keys 'URL', 'Title' and 'Description' (foreach 'site:'-search result). </td></tr>
<tr><td> <code>Google_Backlinks_Total()</code> </td><td> Returns the total amount of results for a Google 'link:'-search on the object URL. </td></tr>
<tr><td> <code>Google_Backlinks_Total_API()</code> <b>new</b> </td><td> Same like Google_Backlinks_Total, but requesting data from the Websearch API. </td></tr>
<tr><td> <code>Google_Backlinks_Array()</code> </td><td> Returns an array, containing the keys 'URL', 'Title' and 'Description' (foreach 'link:'-search result). </td></tr>
<tr><td> <code>Google_Mentions_Total()</code> </td><td> Returns the total amount of results for an exact match Google search on the object URL. </td></tr>
<tr><td> <code>Google_Mentions_Array()</code> </td><td> Returns an array, containing the keys 'URL', 'Title' and 'Description' (foreach exact match result). </td></tr>
<tr><td> <code>Google_Performance_Analysis()</code> </td><td> Returns an array, containing a bunch of technical details about the object URL. </td></tr>
<tr><td> <code>Google_Pagespeed_Score()</code> </td><td> Returns an integer (between 0 - 100). </td></tr></tbody></table>

<hr />
<h3>Yahoo Methods</h3>

<table><thead><th> <b>Method</b> </th><th> <b>@return</b> </th></thead><tbody>
<tr><td> <code>Yahoo()</code> </td><td> Returns an array, containing all results of all Yahoo methods. </td></tr>
<tr><td> <code>Yahoo_Siteindex_Total()</code> </td><td> Returns the total amount of results for a Yahoo 'site:'-search on the object URL. </td></tr>
<tr><td> <code>Yahoo_Siteindex_Array()</code> </td><td> Returns an array, containing the keys 'URL', 'Title' and 'Description' (foreach 'site:'-search result). </td></tr>
<tr><td> <code>Yahoo_Backlinks_Total()</code> </td><td> Returns the total amount of results for a Yahoo 'link:'-search on the object URL. </td></tr>
<tr><td> <code>Yahoo_Backlinks_Array()</code> </td><td> Returns an array, containing the keys 'URL', 'Title' and 'Description' (foreach 'link:'-search result). </td></tr></tbody></table>

<hr />
<h3>Majesticseo Methods</h3>

<table><thead><th> <b>Method</b> </th><th> <b>@return</b> </th></thead><tbody>
<tr><td> <code>Majesticseo()</code> </td><td> Returns an array, containing all results of all Majesticseo methods. </td></tr>
<tr><td> <code>Majesticseo_Siteindex_Total()</code> </td><td> Returns the total amount of indexed pages, listed at Majesticseo. </td></tr>
<tr><td> <code>Majesticseo_Backlinks_Total()</code> </td><td> Returns the total amount of backlinks, listed at Majesticseo. </td></tr>
<tr><td> <code>Majesticseo_Backlinking_Domains_Total()</code> </td><td> Returns the total amount of backlinking domains, listed at Majesticseo. </td></tr>
<tr><td> <code>Majesticseo_Backlinking_IPs_Total()</code> </td><td> Returns the total amount of backlinking IP's, listed at Majesticseo. </td></tr>
<tr><td> <code>Majesticseo_Backlinking_CSubnets_Total()</code> </td><td> Returns the total amount of backlinking Class C subnets, listed at Majesticseo. </td></tr></tbody></table>

<hr />
<h3>Seomoz Methods</h3>

<table><thead><th> <b>Method</b> </th><th> <b>@return</b> </th></thead><tbody>
<tr><td> <code>Seomoz()</code> </td><td> Returns an array, containing all results of all Seomoz methods. </td></tr>
<tr><td> <code>Seomoz_Domainauthority_Array()</code> </td><td> Returns an array, containing the keys 'URL Authority', 'URL mozRank', 'Domain Authority' and 'Domain mozRank'. </td></tr>
<tr><td> <code>Seomoz_Linkdetails_Array()</code> </td><td> Returns an array, containing backlink details by Seomoz. </td></tr></tbody></table>

<hr />
<h3>Alexa Methods</h3>

<table><thead><th> <b>Method</b> </th><th> <b>@return</b> </th></thead><tbody>
<tr><td> <code>Alexa()</code> </td><td> Returns an array, containing all results of all Alexa methods. </td></tr>
<tr><td> <code>Alexa_Global_Rank_Array()</code> </td><td> Returns an array, containing the Alexa Global Rank stats (7d, 1m, 3m). </td></tr>
<tr><td> <code>Alexa_Country_Rank()</code> </td><td> Returns an integer - The (best) local Alexa rank. </td></tr>
<tr><td> <code>Alexa_Rank_By_County()</code> </td><td> Returns an array, containing local Alexa ranks for multiple countries. </td></tr>
<tr><td> <code>Alexa_Visits_By_County()</code> </td><td> Returns an array, containing local visits stats, sorted by country. </td></tr>
<tr><td> <code>Alexa_Pageviews()</code> </td><td> Returns an array, containing pageview stats (7d, 1m, 3m). </td></tr>
<tr><td> <code>Alexa_Pageviews_Per_User()</code> </td><td> Returns an array, containing pageviews per user stats (7d, 1m, 3m). </td></tr>
<tr><td> <code>Alexa_Reach()</code> </td><td> Returns an array, containing reach stats (7d, 1m, 3m). </td></tr>
<tr><td> <code>Alexa_Bounce_Rate()</code> </td><td> Returns an array, containing bounce rate stats (7d, 1m, 3m). </td></tr>
<tr><td> <code>Alexa_Time_On_Site()</code> </td><td> Returns an array, containing time on site stats (7d, 1m, 3m). </td></tr>
<tr><td> <code>Alexa_Search_Visits()</code> </td><td> Returns an array, containing search visit stats (7d, 1m, 3m). </td></tr>
<tr><td> <code>Alexa_Search_Visits_Keywords()</code> </td><td> Returns an array, containing the keywords, refered to the object URL. </td></tr>
<tr><td> <code>Alexa_Search_Visits_Changes()</code> </td><td> Returns an array, containing changes in the keywords, refered to the object URL. </td></tr>
<tr><td> <code>Alexa_Avg_Load_Time()</code> </td><td> Returns a string - the average load time of the object URL. </td></tr>
<tr><td> <code>Alexa_Graph($type='1',$width='660',$height='330',$period='1')</code> </td><td> Returns a string, containing the HTML code of an image, showing Alexa Statistics as Graph.<br>@param  integer  $type  Specifies the graph type. Valid values are 1 to 6. (see below)<br>1 = Daily traffic rank trend<br>2 = Daily pageviews (percent)<br>3 = Daily pageviews per user<br>4 = Time on site (minutes)<br>5 = Bounce rate (percent)<br>6 = Search visits (percent)<br>@param  integer  $width  Specifies the graph width (in px).<br>@param  integer  $height  Specifies the graph height (in px).<br>@param  integer  $period  Specifies the displayed time period. Valid values are 1 to 12.</td></tr></tbody></table>

<hr />
<h3>Facebook Methods</h3>

<table><thead><th> <b>Method</b> </th><th> <b>@return</b> </th></thead><tbody>
<tr><td> <code>Facebook()</code> </td><td> Returns an array, containing all results of all Facebook methods. </td></tr>
<tr><td> <code>Facebook_Mentions_Total()</code> </td><td> Returns an array, containing the total amount of mentions ofthe object URL at Facebook. </td></tr>
<tr><td> <code>Facebook_Mentions_Array()</code> </td><td> Returns an array, containing the keys 'URL', 'Title' and 'Description' (foreach Facebook mention). </td></tr></tbody></table>

<hr />
<h3>Twitter Methods</h3>

<table><thead><th> <b>Method</b> </th><th> <b>@return</b> </th></thead><tbody>
<tr><td> <code>Twitter()</code> </td><td> Returns an array, containing all results of all Twitter methods. </td></tr>
<tr><td> <code>Twitter_Mentions_Total()</code> </td><td> Returns an array, containing the total amount of mentions of the object URL at Twitter. </td></tr>
<tr><td> <code>Twitter_Mentions_Array()</code> </td><td> Returns an array, containing the keys 'URL', 'Title' and 'Description' (foreach Twitter mention). </td></tr></tbody></table>

<hr />
<h3>Other Methods</h3>

<table><thead><th> <b>Method</b> </th><th> <b>@return</b> </th></thead><tbody>
<tr><td> <code>All_Totals()</code> </td><td> Returns an array, containing all results of all methods, but without Linkdetail-Arrays. </td></tr>
<tr><td> <code>Everything()</code> </td><td> Returns an array, containing all results of all methods. </td></tr>
<tr><td> <code>print_array($method,$format)</code> </td><td> Prints an array within <code>&lt;pre&gt;</code> tags.<br>@param  $method  Name of a SEOstats method.<br>@param  $format  This optional parameter can be set to 'json' to receive a json encoded array. </td></tr></tbody></table>

<hr />
<h2>Optional Configurations</h2>

You can adjust some relevant (as i think;)) constants in the <a href='http://code.google.com/p/seostats/#class.seostats.config.php'>class.seostats.config.php</a> file. Note: All changes are <b>optional</b>!<br>
<br>
<hr />
<h1>SEOstats PHP Class</h1>

<h2>class.seostats.php</h2>
<pre><code>&lt;?php<br>
	/**<br>
	 * PHP Class SEOstats<br>
	 *<br>
	 * PHP class to request a bunch of SEO data, such as Backlinkdetails,<br>
	 * Traffic Statistics, Pageauthority and much more.<br>
	 *<br>
	 * ---<br>
	 * @package		class.seostats.2.0.7<br>
	 * @updated		2011/06/11<br>
	 * @author		Stephan Schmitz &lt;eyecatchup@gmail.com&gt;<br>
	 * @copyright	        2010-present, Stephan Schmitz<br>
	 * @license		GNU General Public License (GPL)<br>
	 * @link		http://www.gnu.org/copyleft/gpl.html<br>
	 * @link		http://code.google.com/p/seostats/<br>
	 *<br>
	 * ---<br>
	 * Copyright (c) 2010-present, Stephan Schmitz<br>
	 * All rights reserved.<br>
	 *<br>
	 * Redistribution and use in source and binary forms, with or without<br>
	 * modification, are permitted provided that the following conditions are<br>
	 * met:<br>
	 *<br>
	 *     * Redistributions of source code must retain the above copyright<br>
	 * notice, this list of conditions and the following disclaimer.<br>
	 *     * Neither the name of the Author nor the name of the Product<br>
	 * may be used to endorse or promote products derived from<br>
	 * this software without specific prior written permission.<br>
	 *<br>
	 * THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS<br>
	 * "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT<br>
	 * LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR<br>
	 * A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT<br>
	 * OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,<br>
	 * SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT<br>
	 * LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,<br>
	 * DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY<br>
	 * THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT<br>
	 * (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE<br>
	 * OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.<br>
	 */<br>
<br>
include_once('class.seostats.config.php');<br>
include_once('modules.php');<br>
<br>
class SEOstats<br>
{<br>
	const BUILD_NO 			= '2.0.7';<br>
	const PAGERANK_CHECKSUM_API_URI = 'http://217.150.244.124/prch/?url=';<br>
	<br>
	/**<br>
	 * Object URL<br>
	 *<br>
	 * @access		public<br>
	 * @var			string<br>
	 */<br>
	public $url;<br>
	<br>
	/**<br>
	 * Constructor<br>
	 *<br>
	 * Checks for valid URL syntax and server response.<br>
	 *<br>
	 * @access		public<br>
	 * @param		string		$url		String, containing the initialized <br>
	 *                                                      object URL.<br>
	 */		<br>
	public function __construct($url)<br>
	{<br>
		$this-&gt;url = $url;<br>
		$url_validation = $this-&gt;valid_url($this-&gt;url);<br>
		if($url_validation == 'valid')<br>
		{<br>
			$valid_response_codes = array('200','301','302');<br>
			$curl_result = $this-&gt;get_status_code($this-&gt;url);<br>
			if(in_array($curl_result,$valid_response_codes))<br>
			{<br>
				$this-&gt;host 		= parse_url($this-&gt;url, PHP_URL_HOST);<br>
				$this-&gt;protocol 	= parse_url($this-&gt;url, PHP_URL_SCHEME);<br>
			}<br>
			elseif($curl_result == '0')<br>
			{<br>
				$e = 'Invalid URL &gt; '.$this-&gt;url.' returned no response for a <br>
					HTTP HEAD request, at all. It seems like the Domain does <br>
					not exist.';<br>
				throw new SEOstatsException($e);<br>
			}<br>
			else<br>
			{<br>
				throw new SEOstatsException('Invalid Request &gt; '.$this-&gt;url.<br>
					' returned a '.$curl_result.' status code.');<br>
			}<br>
		}<br>
		else<br>
		{<br>
			throw new SEOstatsException($url_validation);<br>
		}<br>
	}	<br>
<br>
	/**<br>
	 * HTTP GET request with curl.<br>
	 *<br>
	 * @access		private<br>
	 * @param		string		$url		String, containing the URL to <br>
	 *                                                      curl.<br>
	 * @return		string				Returns string, containing the <br>
	 *                                                      curl result.<br>
	 */<br>
	public static function cURL($url)<br>
	{<br>
		$ch  = curl_init($url);<br>
		curl_setopt($ch,CURLOPT_USERAGENT,<br>
			'SEOstats '. SEOstats::BUILD_NO .' code.google.com/p/seostats/');<br>
		curl_setopt($ch,CURLOPT_RETURNTRANSFER,1);<br>
		curl_setopt($ch,CURLOPT_CONNECTTIMEOUT,5);<br>
		curl_setopt($ch,CURLOPT_FOLLOWLOCATION,1);<br>
		curl_setopt($ch,CURLOPT_MAXREDIRS,2);<br>
		if(strtolower(parse_url($url, PHP_URL_SCHEME)) == 'https')<br>
		{<br>
			curl_setopt($ch,CURLOPT_SSL_VERIFYPEER,1);<br>
			curl_setopt($ch,CURLOPT_SSL_VERIFYHOST,1);<br>
		}<br>
		$str = curl_exec($ch);<br>
		curl_close($ch);<br>
<br>
		return $str;   <br>
	}<br>
<br>
	/**<br>
	 * HTTP HEAD request with curl.<br>
	 *<br>
	 * @access		private<br>
	 * @param		string		$url		String, containing the <br>
	 *                                                      initialized object URL.<br>
	 * @return		intval			        Returns a HTTP status code.<br>
	 */		<br>
	private function get_status_code($url)<br>
	{<br>
        $ch = curl_init($url);<br>
		curl_setopt($ch,CURLOPT_USERAGENT,<br>
			'SEOstats '. SEOstats::BUILD_NO .' code.google.com/p/seostats/');<br>
		curl_setopt($ch,CURLOPT_RETURNTRANSFER,1);<br>
		curl_setopt($ch,CURLOPT_NOBODY,1);<br>
		curl_setopt($ch,CURLOPT_CONNECTTIMEOUT,5);<br>
		$str = curl_exec($ch);<br>
		$int = curl_getinfo($ch,CURLINFO_HTTP_CODE);<br>
		curl_close($ch);<br>
		<br>
		return intval($int);<br>
	}<br>
	<br>
	/**<br>
	 * Validates the initialized object URL syntax.<br>
	 *<br>
	 * @access		private<br>
	 * @param		string		$url		String, containing the initialized object URL.<br>
	 * @return		string				Returns string, containing the validation result.<br>
	 */	<br>
	private function valid_url($url)<br>
	{<br>
		$allowed_schemes = array('http','https');<br>
		$host 	= parse_url($url, PHP_URL_HOST);<br>
		$scheme = parse_url($url, PHP_URL_SCHEME);<br>
			<br>
		if(!isset($url) || empty($url) || $url = '')<br>
		{<br>
			$e = 'Invalid Object &gt; Requires an URL.';<br>
		}<br>
		else<br>
		{<br>
			if(!in_array(strtolower($scheme),$allowed_schemes))<br>
			{<br>
				$e = 'Invalid URL &gt; SEOstats supports soley RFC compliant URL\'s with HTTP(/S) protocol.';<br>
			}<br>
			elseif(empty($host) || $host == '')<br>
			{<br>
				$e = 'Invalid URL &gt; Hostname undefined (or invalid URL syntax).';<br>
			}<br>
			else<br>
			{<br>
				/** <br>
				 *  Regex pattern found in and copied from the Nutch source<br>
				 *  @url	{http://nutch.apache.org/}<br>
				 *				 <br>
				 *  Fyi: For the following reason, i decided to stay with preg_match.<br>
				 *<br>
				 *  Testing 10k URL's, returned an average execution time (in seconds, per URL) of:<br>
				 *  if(!preg_match($pattern,$this-&gt;url)) <br>
				 *  0.000104904174805<br>
				 *  if(!filter_var($this-&gt;url, FILTER_VALIDATE_URL, FILTER_FLAG_SCHEME_REQUIRED))<br>
				 *  0.000140905380249<br>
				 */<br>
				$pattern  = '([A-Za-z][A-Za-z0-9+.-]{1,120}:[A-Za-z0-9/](([A-Za-z0-9$_.+!*,;/?:@&amp;~=-])';<br>
				$pattern .= '|%[A-Fa-f0-9]{2}){1,333}(#([a-zA-Z0-9][a-zA-Z0-9$_.+!*,;/?:@&amp;~=%-]{0,1000}))?)';<br>
				if(!preg_match($pattern,$this-&gt;url))<br>
				{<br>
					$e = 'Invalid URL &gt; Invalid URL syntax.';<br>
				}<br>
				else<br>
				{<br>
					$e = 'valid';<br>
				}<br>
			}<br>
		}<br>
		return $e;<br>
	}<br>
	<br>
	/**<br>
	 * Just a 'quicker' way to print an array of a method's  result.<br>
	 *<br>
	 * @param		string		$method		String, containing a method name.<br>
	 * @param		string		$output		Optional Parameter. If set to json, output will be a json encoded array.								 <br>
	 * @access		public<br>
	 * @return		string				Prints an array within &lt;pre&gt; tags.<br>
	 */		<br>
	public function print_array($method,$output='')<br>
	{<br>
		$array = ($output != 'json') ? $this-&gt;$method() : json_encode($this-&gt;$method());<br>
			<br>
		print '&lt;pre&gt;';<br>
		print_r ($array);<br>
		print '&lt;/pre&gt;';<br>
	}<br>
<br>
	/** <br>
	 * @access		public<br>
	 * @return		integer				Returns the Google PageRank.<br>
	 */	 <br>
	public function Google_Page_Rank()<br>
	{<br>
		return SEOstats_Google::Google_PR($this-&gt;host);<br>
	}<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of results for a Google 'site:'-search on the object URL.<br>
	 */	<br>
    public function Google_Siteindex_Total()<br>
	{<br>
		$q = urlencode('site:'.$this-&gt;host);<br>
		return SEOstats_Google::googleTotal($q);      <br>
    }<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer					Returns the total amount of results for a Google 'site:'-search on the object URL.<br>
	 */	<br>
    public function Google_Siteindex_Total_API()<br>
	{<br>
		$q = urlencode('site:'.$this-&gt;host);<br>
		return SEOstats_Google::googleTotal2($q);      <br>
    }<br>
	<br>
	/**<br>
	 * Limited to 1000 results, due to Google.<br>
	 *<br>
	 * @access		public<br>
	 * @return		array 				Returns array, containing foreach 'site:'-search result the keys 'URL', 'Title' and 'Description'.<br>
	 */	<br>
    public function Google_Siteindex_Array()<br>
	{<br>
		$q = urlencode('site:'.$this-&gt;host);<br>
		return SEOstats_Google::googleArray($q);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of results for a Google 'link:'-search on the object URL.<br>
	 */	<br>
    public function Google_Backlinks_Total()<br>
	{<br>
		$q = urlencode('link:'.$this-&gt;host);<br>
		return SEOstats_Google::googleTotal($q);      <br>
    }<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer					Returns the total amount of results for a Google 'link:'-search on the object URL.<br>
	 */	<br>
    public function Google_Backlinks_Total_API()<br>
	{<br>
		$q = urlencode('link:'.$this-&gt;host);<br>
		return SEOstats_Google::googleTotal2($q);      <br>
    }<br>
	<br>
	/**<br>
	 * Limited to 1000 results, due to Google.<br>
	 *<br>
	 * @access		public<br>
	 * @return		array 				Returns array, containing foreach 'link:'-search result the keys 'URL', 'Title' and 'Description'.<br>
	 */	<br>
    public function Google_Backlinks_Array()<br>
	{<br>
		$q = urlencode('link:'.$this-&gt;host);<br>
		return SEOstats_Google::googleArray($q);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of results for an exact match Google search on the object URL.<br>
	 */	<br>
    public function Google_Mentions_Total()<br>
	{<br>
		$q = urlencode('"'.$this-&gt;host.'" -site:'.$this-&gt;host.'');<br>
		return SEOstats_Google::googleTotal($q);<br>
    }<br>
	<br>
	/**<br>
	 * Limited to 1000 results, due to Google.<br>
	 *<br>
	 * @access		public<br>
	 * @return		array 				Returns array, containing foreach exact match search result the keys 'URL', 'Title' and 'Description'.<br>
	 */	<br>
    public function Google_Mentions_Array()<br>
	{<br>
		$q = urlencode('"'.$this-&gt;host.'" -site:'.$this-&gt;host.'');<br>
		return SEOstats_Google::googleArray($q);<br>
    }<br>
<br>
<br>
	/**<br>
	 * Returns Onsite Optimization Tips (for better page performance) by Google.<br>
	 *<br>
	 * @access	public<br>
	 * @return	array		                        Returns array, containing the page analysis results.<br>
	 */<br>
    public function Google_Performance_Analysis()<br>
	{<br>
		return SEOstats_Google::performanceAnalysis($this-&gt;host);<br>
    }	<br>
<br>
	/**<br>
	 * Returns the Google Pagespeed Score.<br>
	 * Score is between 0 (worst) and 100 (best).<br>
	 *<br>
	 * @access	public<br>
	 * @returun	integer		                        Returns a number between 0 - 100.<br>
	 */<br>
    public function Google_Pagespeed_Score()<br>
	{<br>
		return SEOstats_Google::pagespeedScore($this-&gt;host);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of pages for the domain, indexed at Yahoo!.<br>
	 */	<br>
    public function Yahoo_Siteindex_Total()<br>
	{<br>
		return SEOstats_Yahoo::yahooSiteindexTotal($this-&gt;host);      <br>
    }<br>
	<br>
	/**<br>
	 * Limited to 100 results.<br>
	 *<br>
	 * @access		public<br>
	 * @return		integer				Returns array, containing the keys 'Title', 'URL' and 'Click URL'.<br>
	 */	<br>
    public function Yahoo_Siteindex_Array()<br>
	{<br>
		return SEOstats_Yahoo::yahooSiteindexArray($this-&gt;host);      <br>
    }	<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of backlinks to the domain, listed at Yahoo!.<br>
	 */	<br>
    public function Yahoo_Backlinks_Total()<br>
	{<br>
		return SEOstats_Yahoo::yahooBacklinksTotal($this-&gt;host);      <br>
    }<br>
	<br>
	/**<br>
	 * Limited to 100 results.<br>
	 *<br>
	 * @access		public<br>
	 * @return		integer				Returns array, containing the keys 'URL' and 'Anchortext'.<br>
	 */	<br>
    public function Yahoo_Backlinks_Array()<br>
	{<br>
		return SEOstats_Yahoo::yahooBacklinksArray($this-&gt;host);      <br>
    } 	<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of indexed pages for the object URL, listed at Majesticseo.<br>
	 */	<br>
	public function Majesticseo_Siteindex_Total()<br>
	{<br>
		return SEOstats_Majesticseo::report($this-&gt;url, 6); <br>
	}<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of backlinks, listed at Majesticseo.<br>
	 */	<br>
	public function Majesticseo_Backlinks_Total()<br>
	{<br>
		return SEOstats_Majesticseo::report($this-&gt;url, 3);<br>
	}<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of backlinking domains, listed at Majesticseo.<br>
	 */	<br>
	public function Majesticseo_Backlinking_Domains_Total()<br>
	{<br>
		return SEOstats_Majesticseo::report($this-&gt;url, 1);     <br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of backlinking IP's, listed at Majesticseo.<br>
	 */	<br>
    public function Majesticseo_Backlinking_IPs_Total()<br>
	{<br>
		return SEOstats_Majesticseo::report($this-&gt;url, 4);       <br>
    }<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of backlinking Class C subnets.<br>
	 */	<br>
    public function Majesticseo_Backlinking_CSubnets_Total()<br>
	{<br>
		return SEOstats_Majesticseo::report($this-&gt;url, 5);    <br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns array, containing the keys 'URL Authority', 'URL mozRank', 'Domain Authority' and 'Domain mozRank'.<br>
	 */	<br>
    public function Seomoz_Domainauthority_Array()<br>
	{<br>
		return SEOstats_Seomoz::Seomoz_Authority($this-&gt;host);<br>
    }	<br>
<br>
	/**<br>
	 * Limited to 25 links per source domain, due to using a free API key.<br>
	 *<br>
	 * @access		public<br>
	 * @link		http://apiwiki.seomoz.org/w/page/27002419/Glossary	Response Format, Term Conventions<br>
	 * @return		array				Returns multi-array, containing backlink details.<br>
	 */	<br>
    public function Seomoz_Linkdetails_Array()<br>
	{<br>
		return SEOstats_Seomoz::Seomoz_Links($this-&gt;host);<br>
    }<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the Alexa Global Rank. <br>
	 */	<br>
    public function Alexa_Global_Rank_Array()<br>
	{<br>
		return SEOstats_Alexa::extractSingle('div','id','rank','0',$this-&gt;host,true);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the Alexa Country Rank. <br>
	 */	<br>
    public function Alexa_Country_Rank()<br>
	{<br>
		return SEOstats_Alexa::extractSingle('div','class','data','1',$this-&gt;host,false);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing data from Alexa about the total pageviews.<br>
	 */	<br>
    public function Alexa_Pageviews()<br>
	{<br>
		return SEOstats_Alexa::extractSingle('div','id','pageviews','0',$this-&gt;host,true);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing data from Alexa about pageviews per user.<br>
	 */	<br>
    public function Alexa_Pageviews_Per_User()<br>
	{<br>
		return SEOstats_Alexa::extractSingle('div','id','pageviews_per_user','0',$this-&gt;host,true);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing data from Alexa about the reach.<br>
	 */	<br>
    public function Alexa_Reach()<br>
	{<br>
		return SEOstats_Alexa::extractSingle('div','id','reach','0',$this-&gt;host,true);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing data from Alexa about the bounce rate.<br>
	 */	<br>
    public function Alexa_Bounce_Rate()<br>
	{<br>
		return SEOstats_Alexa::extractSingle('div','id','bounce','0',$this-&gt;host,true);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing data from Alexa about the avg time, users stay on the site.<br>
	 */	<br>
    public function Alexa_Time_On_Site()<br>
	{<br>
		return SEOstats_Alexa::extractSingle('div','id','time_on_site','0',$this-&gt;host,true);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing data from Alexa about visitors from searches.<br>
	 */	<br>
    public function Alexa_Search_Visits()<br>
	{<br>
		return SEOstats_Alexa::extractSingle('div','id','search','0',$this-&gt;host,true);<br>
    }<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing the Visits by Country.<br>
	 */	<br>
    public function Alexa_Visits_By_Country()<br>
	{<br>
		return SEOstats_Alexa::Alexa_VBC($this-&gt;url);<br>
    }	<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing the Alexa Rank, sorted by Country.<br>
	 */	<br>
    public function Alexa_Rank_By_Country()<br>
	{<br>
		return SEOstats_Alexa::Alexa_RBC($this-&gt;url);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing data from Alexa about keywords from search visits.<br>
	 */	<br>
    public function Alexa_Search_Visits_Keywords()<br>
	{<br>
		return SEOstats_Alexa::Alexa_SV_Keywords($this-&gt;url);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing data from Alexa about changes of incoming search terms.<br>
	 */	<br>
    public function Alexa_Search_Visits_Changes()<br>
	{<br>
		return SEOstats_Alexa::Alexa_SV_Changes($this-&gt;url);<br>
    }<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		string				Returns string, containing the average load time of the URL from Alexa.<br>
	 */		<br>
	public function Alexa_Avg_Load_Time()<br>
	{<br>
		return SEOstats_Alexa::Alexa_Load_Time($this-&gt;url);<br>
	}<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @param		integer		$type		Specifies the graph type. Valid values are 1 to 6.<br>
	 * @param		integer		$width		Specifies the graph width (in px).<br>
	 * @param		integer		$height		Specifies the graph height (in px).<br>
	 * @param		integer		$period		Specifies the displayed time period. Valid values are 1 to 12.<br>
	 * @return		string				Returns a string, containing the HTML code of an image, showing Alexa Statistics as Graph.<br>
	 */	<br>
    public function Alexa_Graph($type='1',$width='660',$height='330',$period='1')<br>
	{ <br>
		switch($type)<br>
		{<br>
			case 1: $gtype = 't'; break;<br>
			case 2: $gtype = 'p'; break;<br>
			case 3: $gtype = 'u'; break;<br>
			case 4: $gtype = 's'; break;<br>
			case 5: $gtype = 'b'; break;<br>
			case 6:	$gtype = 'q'; break;<br>
			default:break;<br>
		}   <br>
		$graph  = '&lt;img src="http://traffic.alexa.com/graph?&amp;o=f&amp;c=1&amp;y='.$gtype.'&amp;b=ffffff&amp;n=666666';<br>
		$graph .= '&amp;w='.$width.'&amp;h='.$height.'&amp;r='.$period.'m&amp;u='.$this-&gt;url;<br>
		$graph .= '" width="'.$width.'" height="'.$height.'" alt="Alexa Statistics Graph for '.$this-&gt;url.'" /&gt;';<br>
		<br>
		return $graph;<br>
    }<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of Facebook pages mention the URL.<br>
	 */	<br>
	public function Facebook_Mentions_Total()<br>
	{<br>
		$q = urlencode('site:facebook.com "'.$this-&gt;host.'"');<br>
		return SEOstats_Google::googleTotal($q); <br>
	}<br>
	<br>
	/**<br>
	 * Limited to 1000 results.<br>
	 *<br>
	 * @access		public<br>
	 * @return		array 				Returns array, containing detailed results about Facebook pages mention the URL.<br>
	 */	<br>
    public function Facebook_Mentions_Array()<br>
	{<br>
		$q = urlencode('site:facebook.com "'.$this-&gt;host.'"');<br>
		return SEOstats_Google::googleArray($q);<br>
    }	<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		integer				Returns the total amount of Twitter pages mention the URL.<br>
	 */	<br>
	public function Twitter_Mentions_Total()<br>
	{<br>
		$q = urlencode('site:twitter.com "'.$this-&gt;host.'"');<br>
		return SEOstats_Google::googleTotal($q); <br>
	}<br>
	<br>
	/**<br>
	 * Limited to 1000 results.<br>
	 *<br>
	 * @access		public<br>
	 * @return		array 				Returns array, containing detailed results about Twitter pages mention the URL.<br>
	 */	<br>
    public function Twitter_Mentions_Array()<br>
	{<br>
		$q = urlencode('site:twitter.com "'.$this-&gt;host.'"');<br>
		return SEOstats_Google::googleArray($q);<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing all Google data.<br>
	 */<br>
	public function Google()<br>
	{<br>
		$all = 	array(<br>
					'GOOGLE' =&gt; array(<br>
						'Google_Page_Rank'						=&gt; $this-&gt;Google_Page_Rank(),<br>
						'Google_Siteindex_Total'				=&gt; $this-&gt;Google_Siteindex_Total(),<br>
						'Google_Siteindex_Array'				=&gt; $this-&gt;Google_Siteindex_Array(),<br>
						'Google_Backlinks_Total'				=&gt; $this-&gt;Google_Backlinks_Total(),<br>
						'Google_Backlinks_Array'				=&gt; $this-&gt;Google_Backlinks_Array(),<br>
						'Google_Mentions_Total'					=&gt; $this-&gt;Google_Mentions_Total(),<br>
						'Google_Mentions_Array'					=&gt; $this-&gt;Google_Mentions_Array()<br>
					)			<br>
				);<br>
		return array('OBJECT' =&gt; $this-&gt;url, 'DATA' =&gt; $all);<br>
	}<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing all Yahoo! data.<br>
	 */<br>
	public function Yahoo()<br>
	{<br>
		$all = 	array(<br>
					'YAHOO' =&gt; array(<br>
						'Yahoo_Siteindex_Total'					=&gt; $this-&gt;Yahoo_Siteindex_Total(),<br>
						'Yahoo_Siteindex_Array'					=&gt; $this-&gt;Yahoo_Siteindex_Array(),<br>
						'Yahoo_Backlinks_Total'					=&gt; $this-&gt;Yahoo_Backlinks_Total(),<br>
						'Yahoo_Backlinks_Array'					=&gt; $this-&gt;Yahoo_Backlinks_Array()<br>
					)				<br>
				);<br>
		return array('OBJECT' =&gt; $this-&gt;url, 'DATA' =&gt; $all);			<br>
	}<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing all Majesticseo data.<br>
	 */<br>
	public function Majesticseo()<br>
	{<br>
		$all = 	array(<br>
					'MAJESTICSEO' =&gt; array(<br>
						'Majesticseo_Siteindex_Total'			=&gt; $this-&gt;Majesticseo_Siteindex_Total(),<br>
						'Majesticseo_Backlinks_Total'			=&gt; $this-&gt;Majesticseo_Backlinks_Total(),<br>
						'Majesticseo_Backlinking_Domains_Total'	=&gt; $this-&gt;Majesticseo_Backlinking_Domains_Total(),<br>
						'Majesticseo_Backlinking_IPs_Total'		=&gt; $this-&gt;Majesticseo_Backlinking_IPs_Total(),<br>
						'Majesticseo_Backlinking_CSubnets_Total'=&gt; $this-&gt;Majesticseo_Backlinking_CSubnets_Total()<br>
					)				<br>
				);<br>
		return array('OBJECT' =&gt; $this-&gt;url, 'DATA' =&gt; $all);			<br>
	}<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing all SEOmoz data.<br>
	 */<br>
	public function Seomoz()<br>
	{<br>
		$all = 	array(			<br>
					'SEOMOZ' =&gt; array(<br>
						'Seomoz_Domainauthority_Array'			=&gt; $this-&gt;Seomoz_Domainauthority_Array(),<br>
						'Seomoz_Linkdetails_Array'				=&gt; $this-&gt;Seomoz_Linkdetails_Array()<br>
					)				<br>
				);<br>
		return array('OBJECT' =&gt; $this-&gt;url, 'DATA' =&gt; $all);			<br>
	}	<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing all Alexa data.<br>
	 */<br>
	public function Alexa()<br>
	{<br>
		$all = 	array(<br>
					'ALEXA' =&gt; array(<br>
						'Alexa_Global_Rank_Array'				=&gt; $this-&gt;Alexa_Global_Rank_Array(),<br>
						'Alexa_Country_Rank'					=&gt; $this-&gt;Alexa_Country_Rank(),<br>
						'Alexa_Rank_By_Country'					=&gt; $this-&gt;Alexa_Rank_By_Country(),<br>
						'Alexa_Visits_By_Country'				=&gt; $this-&gt;Alexa_Visits_By_Country(),<br>
						'Alexa_Pageviews'						=&gt; $this-&gt;Alexa_Pageviews(),<br>
						'Alexa_Pageviews_Per_User'				=&gt; $this-&gt;Alexa_Pageviews_Per_User(),<br>
						'Alexa_Reach'							=&gt; $this-&gt;Alexa_Reach(),<br>
						'Alexa_Bounce_Rate'						=&gt; $this-&gt;Alexa_Bounce_Rate(),<br>
						'Alexa_Time_On_Site'					=&gt; $this-&gt;Alexa_Time_On_Site(),<br>
						'Alexa_Search_Visits'					=&gt; $this-&gt;Alexa_Search_Visits(),<br>
						'Alexa_Search_Visits_Keywords'			=&gt; $this-&gt;Alexa_Search_Visits_Keywords(),<br>
						'Alexa_Search_Visits_Changes'			=&gt; $this-&gt;Alexa_Search_Visits_Changes(),<br>
						'Alexa_Avg_Load_Time'					=&gt; $this-&gt;Alexa_Avg_Load_Time()<br>
					)				<br>
				);<br>
		return array('OBJECT' =&gt; $this-&gt;url, 'DATA' =&gt; $all);			<br>
	}<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing all Facebook data.<br>
	 */<br>
	public function Facebook()<br>
	{<br>
		$all = 	array(			<br>
					'FACEBOOK' =&gt; array(<br>
						'Facebook_Mentions_Total'				=&gt; $this-&gt;Facebook_Mentions_Total(),<br>
						'Facebook_Mentions_Array'				=&gt; $this-&gt;Facebook_Mentions_Array()<br>
					)				<br>
				);<br>
		return array('OBJECT' =&gt; $this-&gt;url, 'DATA' =&gt; $all);			<br>
	}	<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing all Twitter data.<br>
	 */<br>
	public function Twitter()<br>
	{<br>
		$all = 	array(			<br>
					'TWITTER' =&gt; array(<br>
						'Twitter_Mentions_Total'				=&gt; $this-&gt;Twitter_Mentions_Total(),<br>
						'Twitter_Mentions_Array'				=&gt; $this-&gt;Twitter_Mentions_Array()<br>
					)				<br>
				);<br>
		return array('OBJECT' =&gt; $this-&gt;url, 'DATA' =&gt; $all);			<br>
	}<br>
	<br>
	/**<br>
	 * Method processing might take a few more seconds!<br>
	 *<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing all data but without Linkdetails.<br>
	 */<br>
	public function All_Totals()<br>
	{<br>
		$all = 	array(<br>
					'GOOGLE' =&gt; array(<br>
						'Google_Page_Rank'						=&gt; $this-&gt;Google_Page_Rank(),<br>
						'Google_Siteindex_Total'				=&gt; $this-&gt;Google_Siteindex_Total(),<br>
						'Google_Backlinks_Total'				=&gt; $this-&gt;Google_Backlinks_Total(),<br>
						'Google_Mentions_Total'					=&gt; $this-&gt;Google_Mentions_Total()<br>
					),<br>
					'YAHOO' =&gt; array(<br>
						'Yahoo_Siteindex_Total'					=&gt; $this-&gt;Yahoo_Siteindex_Total(),<br>
						'Yahoo_Backlinks_Total'					=&gt; $this-&gt;Yahoo_Backlinks_Total()<br>
					),<br>
					'MAJESTICSEO' =&gt; array(<br>
						'Majesticseo_Siteindex_Total'			=&gt; $this-&gt;Majesticseo_Siteindex_Total(),<br>
						'Majesticseo_Backlinks_Total'			=&gt; $this-&gt;Majesticseo_Backlinks_Total(),<br>
						'Majesticseo_Backlinking_Domains_Total'	=&gt; $this-&gt;Majesticseo_Backlinking_Domains_Total(),<br>
						'Majesticseo_Backlinking_IPs_Total'		=&gt; $this-&gt;Majesticseo_Backlinking_IPs_Total(),<br>
						'Majesticseo_Backlinking_CSubnets_Total'=&gt; $this-&gt;Majesticseo_Backlinking_CSubnets_Total()<br>
					),			<br>
					'SEOMOZ' =&gt; array(<br>
						'Seomoz_Domainauthority_Array'			=&gt; $this-&gt;Seomoz_Domainauthority_Array()<br>
					),<br>
					'ALEXA' =&gt; array(<br>
						'Alexa_Global_Rank_Array'				=&gt; $this-&gt;Alexa_Global_Rank_Array(),<br>
						'Alexa_Country_Rank'					=&gt; $this-&gt;Alexa_Country_Rank(),<br>
						'Alexa_Rank_By_Country'					=&gt; $this-&gt;Alexa_Rank_By_Country(),<br>
						'Alexa_Visits_By_Country'				=&gt; $this-&gt;Alexa_Visits_By_Country(),<br>
						'Alexa_Pageviews'						=&gt; $this-&gt;Alexa_Pageviews(),<br>
						'Alexa_Pageviews_Per_User'				=&gt; $this-&gt;Alexa_Pageviews_Per_User(),<br>
						'Alexa_Reach'							=&gt; $this-&gt;Alexa_Reach(),<br>
						'Alexa_Bounce_Rate'						=&gt; $this-&gt;Alexa_Bounce_Rate(),<br>
						'Alexa_Time_On_Site'					=&gt; $this-&gt;Alexa_Time_On_Site(),<br>
						'Alexa_Search_Visits'					=&gt; $this-&gt;Alexa_Search_Visits(),<br>
						'Alexa_Search_Visits_Keywords'			=&gt; $this-&gt;Alexa_Search_Visits_Keywords(),<br>
						'Alexa_Search_Visits_Changes'			=&gt; $this-&gt;Alexa_Search_Visits_Changes(),<br>
						'Alexa_Avg_Load_Time'					=&gt; $this-&gt;Alexa_Avg_Load_Time()<br>
					),<br>
					'FACEBOOK' =&gt; array(<br>
						'Facebook_Mentions_Total'				=&gt; $this-&gt;Facebook_Mentions_Total()<br>
					),<br>
					'TWITTER' =&gt; array(<br>
						'Twitter_Mentions_Total'				=&gt; $this-&gt;Twitter_Mentions_Total()<br>
					)					<br>
				);<br>
		return array('OBJECT' =&gt; $this-&gt;url, 'DATA' =&gt; $all);			<br>
	}<br>
	<br>
	/**<br>
	 * Method processing might take a few more seconds!<br>
	 *<br>
	 * @access		public<br>
	 * @return		array				Returns multi-array, containing all data.<br>
	 */<br>
	public function Everything()<br>
	{<br>
		$google 	= $this-&gt;Google();<br>
		$yahoo 		= $this-&gt;Yahoo();<br>
		$majestics 	= $this-&gt;Majesticseo();<br>
		$seomoz 	= $this-&gt;Seomoz();<br>
		$alexa 		= $this-&gt;Alexa();<br>
		$facebook 	= $this-&gt;Facebook();<br>
		$twitter 	= $this-&gt;Twitter();<br>
		<br>
		$all 		= array($google['DATA'],<br>
							$yahoo['DATA'],<br>
							$majestics['DATA'],<br>
							$seomoz['DATA'],<br>
							$alexa['DATA'],<br>
							$facebook['DATA'],<br>
							$twitter['DATA']<br>
							);<br>
		return array('OBJECT' =&gt; $this-&gt;url, 'DATA' =&gt; $all);			<br>
	}<br>
}<br>
?&gt;<br>
</code></pre>

<hr />

<h2>seostats.google.php</h2>
<pre><code>&lt;?php<br>
	/**<br>
	 *  PHP class SEOstats<br>
	 *<br>
	 *  @class      SEOstats_Google<br>
	 *  @package	class.seostats<br>
	 *  @updated	2011/06/11<br>
	 *  @author	Stephan Schmitz &lt;eyecatchup@gmail.com&gt;<br>
	 *  @copyright	2010-present, Stephan Schmitz<br>
	 *  @license	GNU General Public License (GPL)<br>
	 */<br>
<br>
class SEOstats_Google extends SEOstats {<br>
<br>
	/**<br>
	 * Returns total amount of results for any Google search,<br>
	 * requesting the deprecated Websearch API.<br>
	 *<br>
	 * @access		private<br>
	 * @param		string		$query		String, containing the search query.<br>
	 * @param		string		$tld		String, containing the desired Google top level domain.<br>
	 * @return		integer					Returns a total count.<br>
	 */<br>
	public static function googleTotal2($query)<br>
	{<br>
		$url = 'http://ajax.googleapis.com/ajax/services/search/web?v=1.0&amp;rsz=1&amp;q='.$query;<br>
		$str = SEOstats::cURL($url);<br>
		$data= json_decode($str);<br>
		<br>
		return intval($data-&gt;responseData-&gt;cursor-&gt;estimatedResultCount);<br>
	}<br>
<br>
	/**<br>
	 * Returns total amount of results for any Google search.<br>
	 *<br>
	 * @access		private<br>
	 * @param		string		$query		String, containing the search query.<br>
	 * @param		string		$tld		String, containing the desired Google top level domain.<br>
	 * @return		integer					Returns a total count.<br>
	 */<br>
	public static function googleTotal($query)<br>
	{<br>
		$url = 'http://www.google.'. GOOGLE_TLD .'/custom?num=1&amp;q='.$query;<br>
		$str = SEOstats::cURL($url);<br>
		preg_match_all('#&lt;b&gt;(.*?)&lt;/b&gt;#',$str,$matches);<br>
		$result = (!empty($matches[1][2])) ? $matches[1][2] : '0';<br>
		<br>
		return $result;<br>
	}<br>
	<br>
	/**<br>
	 * Returns array, containing detailed results for any Google search.<br>
	 *<br>
	 * @access		private<br>
	 * @param		string		$query		String, containing the search query.<br>
	 * @param		string		$tld		String, containing the desired Google top level domain.<br>
	 * @return		array 					Returns array, containing the keys 'URL', 'Title' and 'Description'.<br>
	 */<br>
	public static function googleArray($query)<br>
	{<br>
		$result = array ();<br>
		$pages = 1;<br>
		$delay = 0;<br>
		for($start=0;$start&lt;$pages;$start++)<br>
		{<br>
			$url = 'http://www.google.'. GOOGLE_TLD .'/custom?q='.$query.'&amp;filter=0'.<br>
				   '&amp;num=100'.(($start == 0) ? '' : '&amp;start='.$start.'00');<br>
			$str = SEOstats::cURL($url);			<br>
			if (preg_match("#answer=86640#i", $str))<br>
			{<br>
				$e = 'Please read: http://www.google.com/support/websearch/' .<br>
					 'bin/answer.py?&amp;answer=86640&amp;hl=en';<br>
				throw new SEOstatsException($e);<br>
			}<br>
			else<br>
			{<br>
				$html = new DOMDocument();<br>
				@$html-&gt;loadHtml( $str );<br>
<br>
				$xpath = new DOMXPath( $html );<br>
				$links = $xpath-&gt;query( "//div[@class='g']//a" );<br>
				$descs = $xpath-&gt;query( "//td[@class='j']//div[@class='std']" );<br>
				$i = 0;<br>
				foreach ( $links as $link )<br>
				{<br>
					if(!preg_match('#cache#si',$link-&gt;textContent) &amp;&amp; <br>
					   !preg_match('#similar#si',$link-&gt;textContent))<br>
					{<br>
						$result []= array(<br>
							'url' =&gt; $link-&gt;getAttribute('href'), <br>
							'title' =&gt; utf8_decode($link-&gt;textContent), <br>
							'descr' =&gt; utf8_decode($descs-&gt;item($i)-&gt;textContent)<br>
						);<br>
						$i++; <br>
					}<br>
				}					<br>
				if ( preg_match('#&lt;div id="nn"&gt;&lt;\/div&gt;#i', $str) ||<br>
					 preg_match('#&lt;div id=nn&gt;&lt;\/div&gt;#i', $str))<br>
				{<br>
					$pages += 1;<br>
					$delay += 200000;<br>
					usleep($delay);<br>
				}<br>
				else<br>
				{<br>
					$pages -= 1;<br>
				}<br>
			}<br>
		}<br>
		return $result;<br>
	}<br>
	<br>
	public static function performanceAnalysis($uri)<br>
	{<br>
		$url  = 'http://pagespeed.googlelabs.com/run_pagespeed?url='.$uri.'&amp;format=json';<br>
		$str  = SEOstats::cURL($url);<br>
<br>
		return json_decode($str);<br>
	}<br>
<br>
	public static function pageSpeedScore($uri)<br>
	{<br>
		$url  = 'http://pagespeed.googlelabs.com/run_pagespeed?url='.$uri.'&amp;format=json';<br>
		$str  = SEOstats::cURL($url);<br>
		<br>
		$data = json_decode($str);<br>
		return intval($data-&gt;results-&gt;score);<br>
	}<br>
	<br>
	/**<br>
	 * Gets the 'GPR_awesomeHash' of the object URL.<br>
	 *<br>
	 * @access		private<br>
	 * @param 		string 		$url 		String, containing the URL to hash.<br>
	 * @return 		string 					Returns hash.<br>
	 */<br>
    public static function genhash ($url)<br>
	{<br>
		$hash = 'Mining PageRank is AGAINST GOOGLE\'S TERMS OF SERVICE. Yes, I\'m talking to you, scammer.';<br>
		$c = 16909125;<br>
		$length = strlen($url);<br>
		$hashpieces = str_split($hash);<br>
		$urlpieces = str_split($url);<br>
		for ($d = 0; $d &lt; $length; $d++)<br>
		{<br>
			$c = $c ^ (ord($hashpieces[$d]) ^ ord($urlpieces[$d]));<br>
			$c = self::zerofill($c, 23) | $c &lt;&lt; 9;<br>
		}<br>
		return '8' . self::hexencode($c);<br>
	}<br>
<br>
	/**<br>
	 * @return 		integer<br>
	 */<br>
	public static function zerofill($a,$b)<br>
	{<br>
		$z = hexdec(80000000);<br>
		if ($z &amp; $a)<br>
		{<br>
			$a  = ($a&gt;&gt;1);<br>
			$a &amp;= (~$z);<br>
			$a |= 0x40000000;<br>
			$a  = ($a&gt;&gt;($b-1));<br>
		}<br>
		else<br>
		{<br>
			$a = ($a&gt;&gt;$b);<br>
		}<br>
		return $a;<br>
	}<br>
<br>
	/**<br>
	 * @return		string<br>
	 */<br>
	public static function hexencode($str)<br>
	{<br>
		$out  = self::hex8(self::zerofill($str, 24));<br>
		$out .= self::hex8(self::zerofill($str, 16) &amp; 255);<br>
		$out .= self::hex8(self::zerofill($str, 8 ) &amp; 255);<br>
		$out .= self::hex8($str &amp; 255);<br>
<br>
		return $out;<br>
	}<br>
	<br>
	/**<br>
	 * @return 		integer<br>
	 */	<br>
    public static function hex8 ($str)<br>
	{<br>
		$str = dechex($str);<br>
		(strlen($str) == 1 ? $str = '0' . $str: null);<br>
<br>
		return $str;<br>
    }<br>
	<br>
	/**<br>
	 * Gets the Google Pagerank<br>
	 *<br>
	 * @access		private<br>
	 * @return 		integer					Returns the Google PageRank.<br>
	 */<br>
	public static function Google_PR($host)<br>
	{<br>
		$domain = 'http://'.$host;<br>
		if(USE_PAGERANK_CHECKSUM_API == true)<br>
		{<br>
			$str  = SEOstats::cURL( SEOstats::PAGERANK_CHECKSUM_API_URI . $domain );<br>
			$data = json_decode($str);<br>
<br>
			$checksum = $data-&gt;CH;<br>
		}<br>
		else<br>
		{<br>
			$checksum = self::genhash($domain);<br>
		}<br>
		$googleurl  = 'http://toolbarqueries.google.com/search?features=Rank&amp;sourceid=navclient-ff&amp;client=navclient-auto-ff';<br>
		$googleurl .= '&amp;googleip=O;66.249.81.104;104&amp;ch='.$checksum.'&amp;q=info:'.urlencode($domain);<br>
		$out = SEOstats::cURL($googleurl);<br>
		<br>
		$pagerank = trim(substr($out, 9));	<br>
		if (!preg_match('/^[0-9]/',$pagerank))<br>
		{<br>
			$pagerank = 'Failed to generate a valid hash for PR check.';<br>
		}<br>
		return $pagerank;<br>
	}<br>
}<br>
?&gt;<br>
</code></pre>

<hr />

<h2>seostats.yahoo.php</h2>
<pre><code>&lt;?php<br>
	/**<br>
	 *  PHP class SEOstats<br>
	 *<br>
	 *  @class      SEOstats_Yahoo<br>
	 *  @package	class.seostats<br>
	 *  @updated	2011/04/29<br>
	 *  @author	Stephan Schmitz &lt;eyecatchup@gmail.com&gt;<br>
	 *  @copyright	2010-present, Stephan Schmitz<br>
	 *  @license	GNU General Public License (GPL)<br>
	 */<br>
<br>
class SEOstats_Yahoo extends SEOstats {<br>
<br>
	/**<br>
	 * Returns the total amount of pages for a Domain indexed at Yahoo!<br>
	 *<br>
	 * @access		private<br>
	 * @link 		http://developer.yahoo.com/search/siteexplorer/		Get your own application ID here<br>
	 * @return		integer 				Returns the total amount of pages for a Domain indexed at Yahoo!<br>
	 */		<br>
	public static function yahooSiteindexTotal($uri)<br>
	{<br>
		$url  = 'http://search.yahooapis.com/SiteExplorerService/V1/pageData?appid=';<br>
		$url .= YAHOO_APP_ID;<br>
		$url .= '&amp;results=1&amp;output=json&amp;query=http://'.urlencode($uri);<br>
		$str  = SEOstats::cURL($url);<br>
<br>
		$data = json_decode($str);<br>
<br>
		return $data-&gt;ResultSet-&gt;totalResultsAvailable;   <br>
	}<br>
<br>
	/**<br>
	 * Returns array, containing details about the pages indexed at Yahoo!<br>
	 *<br>
	 * @access		private<br>
	 * @link 		http://developer.yahoo.com/search/siteexplorer/		Get your own application ID here<br>
	 * @return		array 					Returns array, containing details about the pages indexed at Yahoo!<br>
	 */		<br>
	public static function yahooSiteindexArray($uri)<br>
	{<br>
		$url  = 'http://search.yahooapis.com/SiteExplorerService/V1/pageData?appid=';<br>
		$url .= YAHOO_APP_ID;<br>
		$url .= '&amp;results=100&amp;output=json&amp;query=http://'.urlencode($uri);<br>
		$str  = SEOstats::cURL($url);<br>
<br>
		$data = json_decode($str);<br>
<br>
		$result = array();<br>
		for($i=0;$i&lt;sizeof($data-&gt;ResultSet-&gt;Result);$i++)<br>
		{<br>
			$result[] =  array( 'Title' =&gt; utf8_decode($data-&gt;ResultSet-&gt;Result[$i]-&gt;Title),<br>
								  'URL' =&gt; $data-&gt;ResultSet-&gt;Result[$i]-&gt;Url,<br>
							'Click URL' =&gt; $data-&gt;ResultSet-&gt;Result[$i]-&gt;ClickUrl);<br>
		}<br>
		return $result;   <br>
	}<br>
	<br>
	/**<br>
	 * Returns the total amount of Backlinks indexed at Yahoo!<br>
	 *<br>
	 * @access		private<br>
	 * @link 		http://developer.yahoo.com/search/siteexplorer/		Get your own application ID here<br>
	 * @return		integer 				Returns the total amount of backlinks indexed at Yahoo!<br>
	 */		<br>
	public static function yahooBacklinksTotal($uri)<br>
	{<br>
		$url  = 'http://search.yahooapis.com/SiteExplorerService/V1/inlinkData?appid=';<br>
		$url .= YAHOO_APP_ID;<br>
		$url .= '&amp;results=1&amp;output=json&amp;query=http://'.urlencode($uri);<br>
		$str  = SEOstats::cURL($url);<br>
<br>
		$data = json_decode($str);<br>
<br>
		return $data-&gt;ResultSet-&gt;totalResultsAvailable;   <br>
	}<br>
	<br>
	/**<br>
	 * Returns an array containing details about the backlinks indexed at Yahoo!<br>
	 *<br>
	 * @access		private<br>
	 * @link 		http://developer.yahoo.com/search/siteexplorer/		Get your own application ID here<br>
	 * @return		array 					Returns an array containing details about the backlinks indexed at Yahoo!<br>
	 */		<br>
	public static function yahooBacklinksArray($uri)<br>
	{<br>
		$url  = 'http://search.yahooapis.com/SiteExplorerService/V1/inlinkData?appid=';<br>
		$url .= YAHOO_APP_ID;<br>
		$url .= '&amp;results=100&amp;output=json&amp;query=http://'.urlencode($uri);<br>
		$str  = SEOstats::cURL($url);<br>
<br>
		$data = json_decode($str);<br>
<br>
		$result = array();<br>
		for($i=0;$i&lt;sizeof($data-&gt;ResultSet-&gt;Result);$i++)<br>
		{<br>
			$result[] = array('URL' =&gt; $data-&gt;ResultSet-&gt;Result[$i]-&gt;Url,<br>
					   'Anchortext' =&gt; utf8_decode($data-&gt;ResultSet-&gt;Result[$i]-&gt;Title));<br>
		}<br>
		return $result;   <br>
	}<br>
}<br>
?&gt;<br>
</code></pre>

<hr />

<h2>seostats.majesticseo.php</h2>
<pre><code>&lt;?php<br>
	/**<br>
	 *  PHP class SEOstats<br>
	 *<br>
	 *  @class      SEOstats_Majesticseo<br>
	 *  @package	class.seostats<br>
	 *  @updated	2011/06/11<br>
	 *  @author	Stephan Schmitz &lt;eyecatchup@gmail.com&gt;<br>
	 *  @copyright	2010-present, Stephan Schmitz<br>
	 *  @license	GNU General Public License (GPL)<br>
	 */<br>
<br>
class SEOstats_Majesticseo extends SEOstats {<br>
<br>
	/**<br>
	 * Helper. Gets the Majesticseo's free report webpage.<br>
	 *<br>
	 * @access		private<br>
	 * @return 		string 					String, containing the curl result of the the Majesticseo webpage.<br>
	 */<br>
	public static function report($uri, $i)<br>
	{<br>
		$tmp = SEOstats::cURL( 'http://www.majesticseo.com/reports/site-explorer/summary/'.<br>
			str_replace('http://', '', $uri) );<br>
<br>
		$dom = new DOMDocument();<br>
		@$dom-&gt;loadHTML($tmp);<br>
		$xpath = new DOMXPath($dom);<br>
<br>
		$p = $xpath-&gt;query("//table//tr//td//p");<br>
<br>
		if($i==1 || $i==3)<br>
		{<br>
			$r = trim($p-&gt;item($i)-&gt;textContent);<br>
		} <br>
		else<br>
		{<br>
			switch($i)<br>
			{<br>
					case 4: $regex = ' Referring IP addresses'; break;<br>
					case 5: $regex = ' are Class C subnets'; break;<br>
					case 6: $regex = ' Indexed URLs'; break;<br>
					default:break;<br>
			}<br>
			foreach ( $p as $paragraph )<br>
			{<br>
				if(preg_match('#'.$regex.'#i',$paragraph-&gt;textContent))<br>
				{<br>
					$r = str_replace($regex,'',$paragraph-&gt;textContent);<br>
				}<br>
			}<br>
		}<br>
		return ($r != '') ? $r : intval('0');<br>
	}<br>
}<br>
?&gt;<br>
</code></pre>

<hr />

<h2>seostats.seomoz.php</h2>
<pre><code>&lt;?php<br>
	/**<br>
	 *  PHP class SEOstats<br>
	 *<br>
	 *  @class      SEOstats_Seomoz<br>
	 *  @package	class.seostats<br>
	 *  @updated	2011/06/11<br>
	 *  @author	Stephan Schmitz &lt;eyecatchup@gmail.com&gt;<br>
	 *  @copyright	2010-present, Stephan Schmitz<br>
	 *  @license	GNU General Public License (GPL)<br>
	 */<br>
<br>
class SEOstats_Seomoz extends SEOstats {<br>
<br>
	/**<br>
	 * Gets domain and URL authority from SEOmoz.<br>
	 *<br>
	 * @access		private<br>
	 * @link 		http://www.seomoz.org/api		The SEOmoz API<br>
	 * @return		array 					Returns array, containing authority data.<br>
	 */	<br>
	public static function Seomoz_Authority($uri)<br>
	{<br>
		// external helper class<br>
		include_once ('ext/SeoMoz/Authenticator.php');<br>
<br>
		$authenticator = new Authenticator();<br>
		$url = urlencode($uri);<br>
		$tmp = SEOstats::cURL('http://lsapi.seomoz.com/linkscape/url-metrics/'.$url.'?'.$authenticator-&gt;getAuthenticationStr());<br>
<br>
		$data = json_decode($tmp);<br>
		<br>
		$result = array('URL Authority' 	=&gt; $data-&gt;upa,<br>
						'URL mozRank' 		=&gt; $data-&gt;umrp,<br>
						'Domain Authority' 	=&gt; $data-&gt;pda,<br>
						'Domain mozRank' 	=&gt; $data-&gt;fmrp<br>
						);<br>
		return $result;<br>
	}<br>
<br>
	/**<br>
	 * Gets Backlinkdetails from SEOmoz.<br>
	 * Limited to 25 links per source domain, due to using a free API key.<br>
	 *<br>
	 * @access		private<br>
	 * @link 		http://www.seomoz.org/api		The SEOmoz API<br>
	 * @return		array 					Returns array, containing linkdetails.<br>
	 */<br>
    public static function Seomoz_Links($uri)<br>
	{<br>
		// external helper classes<br>
		include_once('ext/SeoMoz/Authenticator.php');<br>
		include_once('ext/SeoMoz/LinksService.php');<br>
		include_once('ext/SeoMoz/LinksConstants.php');<br>
		<br>
		$authenticator = new Authenticator();<br>
		$linksService = new LinksService($authenticator);<br>
		$result = $linksService-&gt;getLinks($uri, LINKS_SCOPE_PAGE_TO_PAGE, null, LINKS_SORT_DOMAIN_AUTHORITY, LINKS_COL_URL, 0 , 25);<br>
		<br>
		return (!empty($result)) ? $result : 'No data available.';<br>
	}<br>
}<br>
?&gt;<br>
</code></pre>

<hr />

<h2>seostats.alexa.php</h2>
<pre><code>&lt;?php<br>
	/**<br>
	 *  PHP class SEOstats<br>
	 *<br>
	 *  @class      SEOstats_Alexa<br>
	 *  @package	class.seostats<br>
	 *  @updated	2011/06/11<br>
	 *  @author	Stephan Schmitz &lt;eyecatchup@gmail.com&gt;<br>
	 *  @copyright	2010-present, Stephan Schmitz<br>
	 *  @license	GNU General Public License (GPL)<br>
	 */<br>
<br>
class SEOstats_Alexa extends SEOstats {<br>
<br>
	/**<br>
	 * Helper. Get the Alexa's free report webpage.<br>
	 *<br>
	 * @access		private<br>
	 * @return 		string 					String, containing the curl result of the the Alexa webpage.<br>
	 */<br>
	private static function _alexa($uri)<br>
	{<br>
		$tmp = SEOstats::cURL('http://www.alexa.com/siteinfo/'.$uri);<br>
<br>
		return $tmp;<br>
	}<br>
	<br>
	/**<br>
	 * Extracts a String off of HTML input.<br>
	 *<br>
	 * @access		private<br>
	 *<br>
	 * @param 		string 		$tag 		String, containing the html tag to select<br>
	 * @param 		string 		$attr 		String, containing the attribute used on the WHERE condition<br>
	 * @param 		string 		$value 		String, containing the value used on the WHERE condition<br>
	 * @param 		string 		$site 		Input string<br>
	 * @param 		integer 	$id 		Defines the position of the key, to be returned from the preg_match_all array.<br>
	 *<br>
	 * @return 		string/integer 			Returns an integer or a string.<br>
	 */<br>
	public static function extractSingle($tag,$attr,$value,$id,$uri,$alextract)<br>
	{<br>
		// external helper class<br>
		include_once("ext/htmlsql.class.php");<br>
<br>
		$wsql = new htmlsql();<br>
		$wsql-&gt;connect('string', SEOstats_Alexa::_alexa($uri));<br>
		$wsql-&gt;query('SELECT * FROM '.$tag.' WHERE $'.$attr.' == "'.$value.'"');<br>
		$row = $wsql-&gt;fetch_array();<br>
		<br>
		if($alextract == true)<br>
		{<br>
			return SEOstats_Alexa::alextract($row[$id]['text']);<br>
		}<br>
		elseif($alextract == false)<br>
		{<br>
			return trim(strip_tags($row[$id]['text']));<br>
		}<br>
		elseif($alextract == 'none')<br>
		{<br>
			return $row[$id]['text'];<br>
		}<br>
	}<br>
	<br>
	/**<br>
	 * Extracts an Array off of HTML input.<br>
	 *<br>
	 * @access		private<br>
	 *<br>
	 * @param 		string 		$tag 		String, containing the html tag to select<br>
	 * @param 		string 		$attr 		String, containing the attribute used on the WHERE condition<br>
	 * @param 		string 		$value 		String, containing the value used on the WHERE condition<br>
	 * @param 		string 		$site 		Input string<br>
	 *<br>
	 * @return 		array 					Returns an array of results.<br>
	 */<br>
	public static function extractMulti($tag,$attr,$value,$uri)<br>
	{<br>
		// external helper classs<br>
		include_once("ext/htmlsql.class.php");<br>
<br>
		$wsql = new htmlsql();<br>
		$wsql-&gt;connect('string', SEOstats_Alexa::_alexa($uri));<br>
		$wsql-&gt;query('SELECT * FROM '.$tag.' WHERE $'.$attr.' == "'.$value.'"');<br>
<br>
		$results = array ();<br>
		foreach($wsql-&gt;fetch_array() as $row)<br>
		{<br>
			$results[] = $row['text'];<br>
		}<br>
		return $results;<br>
	}<br>
		<br>
	/**<br>
	 * Gets data off of curled Alexa webpages.<br>
	 *<br>
	 * @access		private<br>
	 * @param 		string 		$str 		String, containing the html source code of Alexa's free result webpage.<br>
	 * @return 		array 					Returns an array of Alexa results.<br>
	 */<br>
    public static function alextract($str)<br>
	{<br>
		$tmpArr = explode('&lt;/td&gt;',$str);<br>
		$replace = array("\r", "\r\n", "\n", "7 day", "Yesterday", "1 month", "3 month");<br>
		$value1 = trim(str_replace($replace,'',strip_tags($tmpArr[3])));<br>
		if ($value1 == '-' || $value1 == '' || empty($value1))<br>
		{<br>
			$value1 = 'No Data available.';<br>
			$change1 = '';<br>
		}<br>
		else<br>
		{<br>
			$change1 = trim(strip_tags($tmpArr[4]));<br>
		}<br>
		$value3 = trim(str_replace($replace,'',strip_tags($tmpArr[6])));<br>
		if ($value3 == '-' || $value3 == '' || empty($value3))<br>
		{<br>
			$value3 = 'No Data available.';<br>
			$change3 = '';<br>
		}<br>
		else<br>
		{<br>
			$change3 = trim(strip_tags($tmpArr[7]));<br>
		}<br>
		<br>
		$month1 = array('value' =&gt; $value1, 'change' =&gt; $change1);<br>
		$month3 = array('value' =&gt; $value3, 'change' =&gt; $change3);<br>
		$result = array('1 Month' =&gt; $month1,'3 Months' =&gt; $month3);<br>
		<br>
		return $result;<br>
    }<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		array					Returns multi-array, containing the Visits by Country.<br>
	 */	<br>
    public static function Alexa_VBC($uri)<br>
	{<br>
		$str = SEOstats_Alexa::_alexa($uri);<br>
		<br>
		preg_match_all('#&lt;img class="dynamic-icon" src="/images/flags/(.*?).png" alt="(.*?)"/&gt;(.*?)&lt;/a&gt;#',$str,$country);<br>
		preg_match_all('#&lt;p class="tc1" style="width:30%; text-align:right;"&gt;(.*?)&lt;/p&gt;#',$str,$percent);<br>
		$result = array();<br>
		$countries = array();<br>
		foreach($country[3] as $tmp)<br>
		{<br>
			$x = trim(str_replace('&amp;nbsp;','',$tmp));<br>
			if(!in_array($x,$countries))<br>
			{<br>
				$countries[] = $x;<br>
			}<br>
		}<br>
		for($i=0;$i &lt; sizeof($countries);$i++)<br>
		{<br>
			$result[] = array('Country' =&gt; trim($countries[$i]), 'Percent of Traffic' =&gt; $percent[1][$i]);<br>
		}<br>
		return $result;<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array					Returns multi-array, containing the Alexa Rank, sorted by Country.<br>
	 */	<br>
    public static function Alexa_RBC($uri)<br>
	{<br>
		$str = SEOstats_Alexa::_alexa($uri);<br>
		<br>
		preg_match_all('#&amp;nbsp;(.*?)&lt;/a&gt;#',$str,$country);<br>
		preg_match_all('#&lt;p class="tc1" style="width:40%; text-align:right;"&gt;(.*?)&lt;/p&gt;#',$str,$rank);<br>
		$result = array();<br>
		for($i=0;$i &lt; sizeof($country);$i++)<br>
		{<br>
			$result[] = array('Country' =&gt; trim($country[1][$i]), 'Rank' =&gt; trim($rank[1][$i]));<br>
		}<br>
		return $result;<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array					Returns multi-array, containing data from Alexa about keywords from search visits.<br>
	 */	<br>
    public static function Alexa_SV_Keywords($uri)<br>
	{<br>
		$tmp = SEOstats_Alexa::extractSingle('div','id','top-keywords-from-search','0',$uri,'none');<br>
		$tmp = explode('style="color:#253759;"&gt;', $tmp);<br>
		$tmp = explode('&lt;tr&gt;', $tmp[2]);<br>
		$result = array();<br>
		for ($i=1;$i&lt;sizeof($tmp);$i++)<br>
		{<br>
			$temp = explode('&lt;/td&gt;',$tmp[$i]);<br>
			$result[] = array(<br>
							'Keyword' =&gt; utf8_decode(trim(strip_tags($temp[1]))), <br>
							'Percent of Search Traffic' =&gt; trim(strip_tags($temp[2])));<br>
		}<br>
		return $result;<br>
    }<br>
	<br>
	/**<br>
	 * @access		public<br>
	 * @return		array					Returns multi-array, containing data from Alexa about changes of incoming search terms.<br>
	 */	<br>
    public static function Alexa_SV_Changes($uri)<br>
	{<br>
		$tmp = SEOstats_Alexa::extractMulti('table','class','dataTable',$uri);<br>
		$tmp_incr = explode('&lt;tr&gt;', $tmp[9]);<br>
		$tmp_decl = explode('&lt;tr&gt;', $tmp[11]);<br>
		<br>
		for ($i=1;$i&lt;sizeof($tmp_incr);$i++)<br>
		{<br>
			$temp_incr = explode('&lt;/td&gt;',$tmp_incr[$i]);<br>
			$result_incr[] =  array(<br>
								'Keyword' =&gt; utf8_decode(trim(strip_tags($temp_incr[1]))),<br>
								'Change in Percent' =&gt; trim(strip_tags($temp_incr[2])));<br>
		}<br>
		for ($i=1;$i&lt;sizeof($tmp_decl);$i++)<br>
		{<br>
			$temp_decl = explode('&lt;/td&gt;',$tmp_decl[$i]);<br>
			$result_decl[] = array(<br>
								'Keyword' =&gt; utf8_decode(trim(strip_tags($temp_decl[1]))),<br>
								'Change in Percent' =&gt; trim(strip_tags($temp_decl[2])));<br>
		}		<br>
		if(empty($result_incr)) { $result_incr = 'No Data available.'; }<br>
		if(empty($result_decl)) { $result_decl = 'No Data available.'; }<br>
		$result = array('Increase' =&gt; $result_incr, 'Decline' =&gt; $result_decl);<br>
		<br>
		return $result;<br>
    }<br>
<br>
	/**<br>
	 * @access		public<br>
	 * @return		string					Returns string, containing the average load time of the URL from Alexa.<br>
	 */		<br>
	public static function Alexa_Load_Time($uri)<br>
	{	<br>
		$str = SEOstats_Alexa::_alexa($uri);	<br>
		$html = new DOMDocument();<br>
		@$html-&gt;loadHtml( $str );<br>
<br>
		$xpath = new DOMXPath( $html );<br>
		$p = $xpath-&gt;query( "//div[@class='speedAd']//div//p" );<br>
		foreach($p as $match)<br>
		{<br>
			if(preg_match('/Seconds/si',$match-&gt;textContent))<br>
			{<br>
				return trim(strip_tags($match-&gt;textContent));<br>
				exit();<br>
			}<br>
		}<br>
		return 'No data available.';<br>
	}<br>
}<br>
?&gt;<br>
</code></pre>

<hr />

<h2>seostats.exception.php</h2>
<pre><code>&lt;?php<br>
	/**<br>
	 *  PHP class SEOstats<br>
	 *<br>
	 *  @package	class.seostats<br>
	 *  @updated	2011/04/29<br>
	 *  @author	Stephan Schmitz &lt;eyecatchup@gmail.com&gt;<br>
	 *  @copyright	2010-present, Stephan Schmitz<br>
	 *  @license	GNU General Public License (GPL)<br>
	 *<br>
	 *  EXCEPTION<br>
	 */<br>
<br>
class SEOstatsException extends Exception {}	 <br>
	 <br>
if (!function_exists('curl_init'))<br>
{<br>
	throw new SEOstatsException('SEOstats needs the PHP CURL extension.');<br>
}<br>
if (!function_exists('json_decode'))<br>
{<br>
	throw new SEOstatsException('SEOstats needs the PHP JSON extension.');<br>
}<br>
?&gt;<br>
</code></pre>

<hr />

<h2>class.seostats.config.php</h2>
<pre><code>&lt;?php<br>
	/**<br>
	 *  PHP class SEOstats<br>
	 *<br>
	 *  @package	class.seostats<br>
	 *  @updated	2011/04/29<br>
	 *  @author	Stephan Schmitz &lt;eyecatchup@gmail.com&gt;<br>
	 *  @copyright	2010-present, Stephan Schmitz<br>
	 *  @license	GNU General Public License (GPL)<br>
	 *<br>
	 *  GLOBALS<br>
	 */<br>
 <br>
	define('GOOGLE_TLD', <br>
		'com');<br>
	define('USE_PAGERANK_CHECKSUM_API', <br>
		false);<br>
<br>
	/**<br>
	 *  Optional changes.<br>
	 */<br>
	define('YAHOO_APP_ID', <br>
		'oVFwwjnV34GEEZTLB3K_WW1YC9_VysYbCYQ4szoXTAHZscrDvMazUpFR7TR0wchmlA--');<br>
	<br>
	define('SEOMOZ_ACCESS_ID', <br>
		'member-881a55bcfb');<br>
	define('SEOMOZ_SECRET_KEY', <br>
		'7145d56a1279285be92e6e4875bba8ee');<br>
?&gt;<br>
</code></pre>

<hr />

<h2>modules.php</h2>
<pre><code>&lt;?php<br>
	/**<br>
	 *  PHP class SEOstats<br>
	 *<br>
	 *  @package	class.seostats<br>
	 *  @updated	2011/04/29<br>
	 *  @author	Stephan Schmitz &lt;eyecatchup@gmail.com&gt;<br>
	 *  @copyright	2010-present, Stephan Schmitz<br>
	 *  @license	GNU General Public License (GPL)<br>
	 *<br>
	 *  SEOstats modules<br>
	 */<br>
 <br>
include_once('seostats.google.php');<br>
include_once('seostats.yahoo.php');<br>
include_once('seostats.majesticseo.php');<br>
include_once('seostats.seomoz.php');<br>
include_once('seostats.alexa.php');<br>
include_once('seostats.exception.php');<br>
?&gt;<br>
</code></pre>

<hr />

<h1>Changelog</h1>
<pre><code>/*<br>
 ======================================================================<br>
 CHANGELOG<br>
 ----------------------------------------------------------------------<br>
 v2.0.7       11.06.2011    * added method Google_Siteindex_Total_API<br>
                            * added method Google_Backlinks_Total_API<br>
                            * fixed Majesticseo methods<br>
                            * fixed method Seomoz_Linkdetails_Array<br>
                            * fixed method Alexa_Avg_Load_Time<br>
                            * improved method googleArray by changing<br>
                              from regular expressions to xpath <br>
 v2.0.6       18.05.2011    * added method Google_Performance_Analysis<br>
                            * added method Google_Pagespeed_Score<br>
                            * fixed method googleArray<br>
                            * fixed typo in method print_array<br>
 v2.0.5       29.04.2011    * fixed method googleArray<br>
			    * improved regex pattern for URL validation<br>
 v2.0.4       13.04.2011    * fixed method Google_Backlinks_Array<br>
                            * improved method googleArray<br>
                              * no more need of external helper classes<br>
                              * added a delay when scraping more than 100 results at once<br>
                            * removed the Google Pagerank API<br>
                            * added a Pagerank Checksum API<br>
 v2.0.3       13.03.2011    * fixed all Majesticseo methods<br>
                            * added method Majesticseo_Backlinking_CSubnets_Total<br>
 v2.0.2       18.02.2011    * added method Alexa_Visits_By_Country<br>
 v2.0.1       18.02.2011    * added method Alexa_Rank_By_Country<br>
                            * added method Alexa_Avg_Load_Time<br>
 v2.0         17.02.2011    * Major code clean up<br>
                            * improved existing methods<br>
                            * added new Yahoo methods<br>
                            * added new SEOmoz methods<br>
                            * added new Facebook methods<br>
                            * added new Twitter methods<br>
                            * added optional Pagerank API<br>
                            * added optional json output method<br>
                            * removed GUI example<br>
 v1.2.3       18.12.2010    * fixed method PageRank<br>
 v1.2.2       17.12.2010    * improved method AlexaGlobalRank<br>
                              * pure numeric result<br>
                              * no more html in output<br>
                            * improved method AlexaCountryRank<br>
                              * pure numeric result<br>
                              * no more html in output<br>
                            * improved Alexa Stats and Trend methods<br>
                              * no more html wrapped output<br>
                              * returns results as array<br>
 v1.2.1       09.12.2010    * fixed method GoogleLinks<br>
 v1.2         01.12.2010    * added new Google methods<br>
                              * GoogleIndexDetails<br>
                              * GoogleLinkDetails<br>
                              * GoogleMentions<br>
                            * Introduced global var $google_tld<br>
                              * used in all google methods<br>
                              * if not defined = com<br>
                            * enhanced method GoogleIndex<br>
                              * No longer requires an API Key<br>
                            * enhanced method GoogleLinks<br>
                              * No longer requires an API Key<br>
 v1.1         29.10.2010    * added Yahoo methods<br>
                              * YahooLinks<br>
                              * YahooLinkDetails<br>
 v1.0.3       19.10.2010    * fixed method AlexaCountryRank<br>
 v1.0.2       19.10.2010    * added method PageRank<br>
 v1.0.1       19.10.2010    * added method cURL<br>
 ----------------------------------------------------------------------<br>
 ======================================================================<br>
*/<br>
</code></pre>

<hr />

<h1>Roadmap</h1>
v2.1  June 2011<br>
<ul><li>New methods to gather detailed user demographics.<br>
</li><li>New methods to gather data from several bookmarking Services<br>
</li><li>More detailed methods for social media data</li></ul>

<hr />
<h1>Google Pagerank API Info</h1>
Due to heavy misuse (coming from the Harvard University Network), i needed to shut down the Google Pagerank API.<br>
<br>
The soley purpose of the "API" was to give all users the same chance to request the Pagerank for a site - eventhough they can not generate a valid checksum for the PR request on their own machines.<br>
<br>
Thus i changed the <code>$use_pagerank_api</code> parameter of the class to <code>$use_pr_checksum_api</code> with the release of v2.0.4. So you can use the new "API" to get the checksum, but the actual request to the google servers need to be done by yourself.